# 주차별 구현내용 (1~6주차)
---
### 1주차
---
#### step1

- Product 클래스 생성 후 캡슐화
- ProductController에 RestController 어노테이션 적용 후 정보 저장용 Map구조 생성
- GetMapping어노테이션으로 메소드 생성 후 저장된 Product 객체들을 리스트형태로 반환하는 기능 구현
- PostMapping어노테이션으로 메소드 생성 후 RequestBody로 받은 JSON데이터를 Product객체로 만들고 해당 객체의 id를 1씩 증가시켜 리턴하는 기능 구현
- PutMapping어노테이션으로 메소드 생성 후 PathVariable에 해당하는 id의 데이터가 존재하는지 확인하고 전달받은 JSON데이터를 변환하여 객체 데이터를 수정하고 리턴하는 기능 구현
- DeleteMapping어노테이션으로 메소드 생성 후 PathVariable로 전달받은 id값에 해당하는 데이터가 존재하는지 확인 후 해당 데이터를 삭제하는 기능 구현
> step1 종료

#### step2
- 관리자 페이지 생성을 위해 ProductAdminController생성, @Controller 어노테이션 적용
- CRUD기능 html리턴타입으로 생성
- 관리자 페이지 html 생성
> step2 종료

#### step3
- 데이터베이스 설정 (application.properties)
- 데이터베이스 테이블 생성
- controller를 Dao, Service, controller로 분리 및, 의존성 주입

> step3 종료

<br>

---
### 2주차
---
#### step1

- Validation 종속성 추가
- DTO에 검증 값 어노테이션 추가
- Controller 수정 및 GlobalExceptionHandler에서 오류 message 처리
- 서버 사이드 렌더링(관리자 화면)에서 입력 오류 처리기능 추가
> step1 종료

#### step2

- id, email, password 필드를 가진 엔티티 클래스 생성
- UserRepository DAO생성하여 DB 연동
- 인증 Request, Response DTO 생성 및 구현
- 랜덤 토큰을 생성하는 TokenService 클래스 생성 및 구현
- 보일러 플레이트를 피하기 위해 Interceptor 생성 및 구현
- Interceptor 의존성을 주입한 WebConfig 생성 및 구현
- schema에 users 테이블 추가
- AuthController 구현
> step2 종료

#### step3

- wish entity 생성 및 스키마 작성
- wish의 request를 다룰 DTO 생성 및 구현
- 데이터를 access할 wish DAO 생성 및 구현
- 비즈니스 로직을 처리할 wish Service 및 User Service 생성 및 구현
- 컨트롤러 메서드에 진입 전 로그인 유저 객체를 주입하기 위한 기능 구현
- wish 리스트를 다룰 컨트롤러 생성 구현
> step3 종료

<br>

---
### 3주차
---

#### step1

- 필요 의존성 추가 및 properties 추가
- 각 entity JPA로 변환
- Repository class 생성 및 구현
- @DataJpaTest를 이용한 Test생성 및 구현
> step1 종료

#### step2

- entity들 연관관계 매핑
- 매핑된 연관관계 기반 외래 키 사용으로 코드 수정
- Test코드 수정 및 테스트
> step2 종료

#### step3

- JPA repository에 Page타입의 find JPQL 추가
- service와 repository단 모든 객체 표시 반환 타입을 List -> Page로 변경
- test를 위한 더미 데이터 추가
- test코드 추가
> step3 종료

<br>

---
### 4주차
---

#### step1

- 카테고리 엔티티 및 DTO 생성
- Product와 연관관계 생성
- 카테고리를 다루는 repository, service와 controller 생성 및 구현
- 추가된 부분 기반 전체적 코드 수정
- 카테고리 repository 테스트 생성 및 구현
- E2E 테스트 및 엔티티 테스트 추가
> step1 종료

#### step2

- 옵션 엔티티 및 DTO 생성
- Product와 연관관계 생성
- 옵션 Vaild 설정
- 옵션을 다루는 repostiory, service와 controller 생성 및 구현
- 옵션 repository, entity 테스트 생성 및 구현
- 관리자 페이지 옵션 기능 추가
> step2 종료

#### step3

- Option entity에 상품 옵션의 수량 빼는 메서드 추가
- 뺄 quantity를 입력받는 레코드 타입의 DTO 추가
- OptionService에서 비즈니스 로직 구현
- OptionController에서 실행 메서드 구현
- E2E 테스트와 Entity 테스트에 추가된 기능 테스트 추가
> step3 종료

<br>

---
### 5주차
---
#### step1

- 앱 키를 새로운 properties파일에 설정하고 gitignore 등록
- 앱 키를 로드할 KakaoProperties 구현
- 카카오 로그인을 담당할 Service, Controller 구현
- 테스트코드 추가
> step1 종료

#### step2

- accessToken에서 이메일 정보 추출 로직 구현
- 추출한 이메일 정보를 바탕으로 회원가입 or 로그인 기능 구현
- 주문 entity 및 DTO 생성
- 주문 로직 구현
- 카카오 메세지 전송 기능 구현
> step2 종료

#### step3

- api 명세 작성 (swagger 사용)
> step3 종료

<br>

---
### 6주차
---
#### step1

- API 명세 통일하기
> step1 종료

#### step2

- 배포 스크립트 작성
- 보안 문제 대응
- 협업을 위한 지속적 의논 및 수정
> step2 종료

#### step3

- 유저에 포인트 필드 추가
- 포인트 로직 추가 및 예외처리
> step3 종료
