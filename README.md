# SPRING PLUS
## 1. 코드 개선 퀴즈 - @Transactional의 이해

- 할 일 저장 기능을 구현한 API(`/todos`)를 호출할 때, 아래와 같은 에러가 발생합니다:

- **에러 로그 원문**:
    ```
    jakarta.servlet.ServletException: Request processing failed: org.springframework.orm.jpa.JpaSystemException: 
    could not execute statement [Connection is read-only. Queries leading to data modification are not allowed] 
    [insert into todos (contents,created_at,modified_at,title,user_id,weather) values (?,?,?,?,?,?)]
    ```

- **해결 요구사항**: 에러가 발생하지 않고 정상적으로 할 일을 저장할 수 있도록 코드를 수정해주세요.

---

## 2. 코드 추가 퀴즈 - JWT의 이해

🚨 **기획자의 긴급 요청**  
아래 요구사항에 맞춰 기획 요건을 충족하는 코드를 작성해주세요.

- **요구사항**:
    - `User`의 정보에 `nickname`이 필요합니다.
    - `nickname`은 중복 가능하도록 설정해주세요.
    - JWT에서 유저의 `nickname`을 꺼내서 프론트엔드 화면에 보여주도록 처리해주세요.

---

## 3. 코드 개선 퀴즈 - AOP의 이해

😱 **AOP가 잘못 동작하고 있어요!**

- `UserAdminController` 클래스의 `changeUserRole()` 메소드가 실행 전 동작하도록 수정해야 합니다.
- `AdminAccessLoggingAspect` 클래스의 AOP가 의도한 대로 작동하도록 코드를 수정해주세요.

---

## 4. 테스트 코드 퀴즈 - 컨트롤러 테스트의 이해


- 테스트 패키지 `org.example.expert.domain.todo.controller`에서  
  `todo_단건_조회_시_todo가_존재하지_않아_예외가_발생한다()` 테스트가 실패하고 있습니다.

- **해결 요구사항**: 테스트가 정상적으로 통과할 수 있도록 테스트 코드를 수정해주세요.

---

## 5. 코드 개선 퀴즈 - JPA의 이해


🚨 **기획자의 긴급 요청**  
아래 요구사항에 맞춰 기획 요건을 충족하는 코드를 작성해주세요.

- 할 일 검색 시 `weather` 조건을 추가해야 합니다. 이 조건은 있을 수도 없을 수도 있습니다.
- 할 일 검색 시 수정일을 기준으로 기간 검색이 가능해야 합니다.
- **주의**: 기간의 시작과 끝 조건도 선택적입니다.
- **사용해야 할 기술**: JPQL을 사용하며, 쿼리 메소드명은 짧게 설정해주세요.

---

## 6. JPA Cascade & 7. N+1 문제


- `CommentController`의 `getComments()` API 호출 시 **N+1 문제가 발생**하고 있습니다.
- **N+1 문제**란, 연관된 엔티티를 조회할 때 발생하는 쿼리 성능 저하 문제입니다.
- **해결 요구사항**:
    - JPQL로 작성된 `findByIdWithUser`를 QueryDSL로 변경해주세요.
    - N+1 문제가 발생하지 않도록 유의하여 코드를 수정해주세요.

---

### 7. N+1 문제


- `CommentController` 클래스의 `getComments()` API를 호출할 때 **N+1 문제**가 발생하고 있습니다.  
- **N+1 문제**란, 연관된 엔티티를 조회할 때 데이터베이스 쿼리 성능 저하를 일으키는 대표적인 문제 중 하나입니다.
    - 특히 여러 개의 연관 엔티티를 한번에 조회할 때, 각 엔티티에 대해 개별 쿼리가 발생하면서 성능 저하가 일어납니다.
- **해결 요구사항**: N+1 문제가 발생하지 않도록 코드를 개선해주세요.

---

## 8. QueryDSL 적용

- `TodoService.getTodo` 메소드에서 사용된 JPQL로 작성된 `findByIdWithUser` 메소드를 **QueryDSL**로 변경해주세요.
- **7번 문제와 동일하게 N+1 문제가 발생하지 않도록** 주의하여 코드 개선을 진행해주세요.

---
## 9. Spring Security 적용

⚙️ **Spring Security 도입**  
기존 `Filter`와 `Argument Resolver`를 사용하던 코드를 Spring Security로 변경하세요.

- **요구사항**:
    - 기존의 접근 권한 및 유저 권한 기능을 유지하며 Spring Security의 기능을 사용하세요.
    - 토큰 기반 인증 방식인 JWT는 그대로 사용하세요.


