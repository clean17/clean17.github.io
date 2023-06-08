# 블로그 프로젝트 
![blogmain](https://user-images.githubusercontent.com/118657689/236416188-deddb0b0-081a-4ec8-b76d-d6a07ff99793.jpg)


> ## 개발 목표

- DB를 설계하고 연관관계를 파악해서 기본적인 CRUD 쿼리를 작성해본다
- 블로그의 로직을 이해하고 필요한 기능 및 추가되면 좋을 기능을 생각해서 추가해본다.
- 단위 테스트를 하는것에 익숙해진다.

<br>

> ## 개발 환경

- Visual Studio Code
- Java 11


<br>

> ## 기술 스택

- JDK 11
- Spring Boot 2.7.8
- MyBatis
- 테스트 h2 DB
- 프로덕션 MySql DB
- JSP
- JUnit


<br>

> ## 기능정리

### 1단계
- 회원 가입, 로그인, 글 쓰기, 글 목록보기 (썸네일 제외), 글 상세보기, 글 삭제 , 글 수정, 썸네일
### 2단계
- 댓글 쓰기, 댓글 목록보기, 댓글 삭제, 프로픽 사진 추가
### 3단계
- 좋아요 버튼, 좋아요 갯수
### 4단계
- 아이디 중복체크, 회원수정하기
### 5단계
- 관리자 추가, 검색, 이메일

<br>

> ## 의존성 주입

	implementation 'org.springframework.boot:spring-boot-starter-mail'
	implementation 'org.jsoup:jsoup:1.15.3'
	implementation group: 'com.google.code.gson', name: 'gson', version: '2.8.9'
	implementation 'javax.servlet:jstl'
    implementation 'org.apache.tomcat.embed:tomcat-embed-jasper'
	implementation 'org.springframework.boot:spring-boot-starter-web'
	implementation 'org.springframework.boot:spring-boot-starter-aop'
	implementation 'org.mybatis.spring.boot:mybatis-spring-boot-starter:2.3.0'
	compileOnly 'org.projectlombok:lombok'
	developmentOnly 'org.springframework.boot:spring-boot-devtools'
	runtimeOnly 'com.h2database:h2'
	annotationProcessor 'org.projectlombok:lombok'
	testImplementation 'org.springframework.boot:spring-boot-starter-test'
	testImplementation group: 'org.mybatis.spring.boot', name: 'mybatis-spring-boot-starter-test', version: '2.2.2'


<br>

> ## 테이블 모델링

![블로그 DB 설계](https://user-images.githubusercontent.com/118657689/236416233-ac5417f1-c25e-4f35-82be-c18e9c9719b8.jpg)

<br>

> ## 적용된 기능

  - 회원가입, 로그인 <br>
  - 아이디, 비밀번호 중복확인<br>
  - 글 목록 보기, 글 쓰기, 수정, 삭제<br>
  - 등록한 첫번째 사진으로 블로그 썸네일 <br>
  - AJAX 비동기로 댓글 쓰기, 삭제 <br>
  - 프로필 사진 변경 <br>
  - 좋아요 수 증가, 감소 <br>
  - 관리자 페이지( 검색, 삭제, 이메일 전송) <br />
  - Sha256 비밀번호 암호화<br>
  - Junit5 단위테스트<br>
  - 인터셉터로 인증처리<br>

<br>

> ## 이슈

- 좋아요 기능을 구현하려고 할때 테이블에서 삭제하지 않고 상태값만 변하게 만들고 싶었는데 여러 환경마다 방법이 달라서 시행착오 끝에 지금 환경에서는 useGenerateKey를 사용해서 id를 리턴하면 손쉽게 좋아요상태를 update할 수 있었다.

<br>

> ## 기술 블로그


- <a href="https://velog.io/@merci/series/%EB%B8%94%EB%A1%9C%EA%B7%B8-%EC%A0%9C%EC%9E%91-V1"> 블로그 링크 </a>
