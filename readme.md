## 자바 웹 총정정리
- 자바는 객체지향, 모듈화를 추구한다, 대기업에서의 분업을 위한 언어 
## Client
- language
  - java script : html에 동적 요소를 추가 하기 위함
  - jquery : java script를 편하게 쓰기 위한 라이브러리
  - html : 간단한 이벤트, 글
  - css : 꾸며주기
- operation
  - 동기 방식 / 어떠한 이벤트가 발생하면 (클릭, 엔터 등등) request를 서버로 보냄
  - Ajax (비동기 방식)
    - html은 그대로 두고 data만 보냄, 이를 서버에서 처리하고 data를 받아서 기존의 html에 추가함 
## Server
- Tomcat 
  - 소켓 통신을 담당함
  - 클라이언트에서 받은 데이터를 request 객체 형태로 만들어줌
  - container역할, servelet들을 가지고 있음
  - 내장 객체 response request 등등을 가지고 있고 이를 선언함
- servelet
  - 백앤드 개발자가 주로 개발하는 부분
  - 톰캣이 만들어준 request 객체를 바탕으로 여러가지 작업을함
  - response 객체를 만들어서 톰캣에게 넘겨줌
- DAO 
  - servelet 의 요청을 받아 데이터 베이스와 관련된 작업, sql문 실행해서 데이터 가져오거나 비교하는 등의 작업을 함
  - 다시 servlet에게 데이터 넘겨줌
- model 

- MVC 패턴 
  - Model
  - View
    -
  - Controller
    - 이부분을 현재 servelet이 담당하지만 후에는 Controller가 담당
## database

