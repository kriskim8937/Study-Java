## 자바 웹 총정정리
- 자바는 객체지향, 모듈화를 추구한다, 대기업에서의 분업을 위한 언어 
- 디자인 패턴 추가는 할 수 있되 기존의 것은 안 바뀌었으면 좋겠음(수정되면 문제가 생김)
## Client
- language
  - java script : html에 동적 요소를 추가 하기 위함
  - jquery : java script를 편하게 쓰기 위한 라이브러리
  - html : 간단한 이벤트, 글
  - css : 꾸며주기
- operation
  - 동기 방식 / 어떠한 이벤트가 발생하면 (클릭, 엔터 등등) request객체 안에 parameter 들을 넣어서 서버로 보냄
  - Ajax (비동기 방식)
    - html은 그대로 두고 data만 보냄, 이를 서버에서 처리하고 data를 받아서 기존의 html에 추가함 
## Server
- Tomcat 
  - 소켓 통신을 담당함
  - 클라이언트에서 받은 데이터를 request 객체 형태로 만들어줌
  - container역할, servelet들을 가지고 있음
  - 내장 객체 response request 등등을 가지고 있고 이를 선언함
  - response 객체의 데이터를 클라이언트로 보내줌 
- servelet
  - jsp와 servlet의 관계 https://gmlwjd9405.github.io/2018/11/04/servlet-vs-jsp.html
  - 백앤드 개발자가 주로 개발하는 부분
  - 톰캣이 만들어준 request 객체를 바탕으로 여러가지 작업을함
  - response 객체에 그러한 작업을 저장함 톰캣에게 넘겨줌
  - 흐름 컨트롤 
- service
  - 실질적인 로직 담당, 무언가 판단
  - servlet 이 할일이 많아서 분업함
  - insert select 등의 db 작업은 DAO에게 맞김 
- DAO 
  - servelet(controller) 의 요청을 받아 데이터 베이스와 관련된 작업, sql문 실행해서 데이터 가져오거나 비교하는 등의 작업을 함
  - 다시 servlet(controller)에게 데이터 넘겨줌
  - 로직을 수행하는 것은 아님 
- model 
  - 요청의 흐름과 상관 없이 데이터를 가지고 있는 객체 자체
  - 데이터 가공

- MVC 패턴 - 사람마다 정의가 약간씩 다르다. 
  - https://m.blog.naver.com/jhc9639/220967034588
  - Model 데이터 베이스나 파일과 같은 데이터 소스를 제어(DML) 한후에 그결과를 리턴한다.
    - model
    - service
    - dao
  - View - controller가 model이 리턴한 결과를 view에 반영하고 이를 웹서버를 통해 클라이언트로 response해 사용자에게 보여준다.
    - 주로 JSP로 이루어져 있다. (JSP는 HTML상에서 JAVA를 사용하기 때문에 이에 적합하다)
  - Controller 사용자가 용청한 웹페이지를 서비스 하기 위해 모델을 호출한다.
    - 이부분을 현재 servelet이 담당하지만 후에는 Controller가 담당
    - receive
    - interpret & valisate input
    - create & update views;
    - query & modify models; 모델에게 데이터를 요구
    - 주로 servelet으로 이루어져 있다. (servelet은 JAVA상에서 HTML을 사용하기 때문에 이에 적합하다)
## database
- Mysql
  - scheme
  - table
  - statements
## Web server
- HTML 같은 정적 데이터를 처리하는 서버 정적 데이터의경우 was보다 처리가 빠르고 안정적
## WAS
- Web server + Serice / 동적 데이터를 처리하는 서버 데이터베이스와 연결, MVC패턴이 들어갈 수 있음
## Reference
- https://welin.tistory.com/5
