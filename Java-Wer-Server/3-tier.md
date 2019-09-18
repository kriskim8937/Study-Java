# 3-teir
- Client Tier
  - stateless + sync(request and response) : 브라우저가 아무일도 안하고 서버에서 답이 올때까지 기다림
  - Async : 동시에 할수 있게 해줌 XHR, AJAX, open, send, call back
  - Front End
    - data type : Json(key:value), Xml(tag), p 
  - HTML:Structure
  - CSS : Style
    - Selector (.,#,A B,A>B,A+B)
  - JS(JQery):function
  - Dom -> 
- Server Tier
  - 3 Layer
    - Presentation layer 
      - view
      - jsp : for문 도는 이유 -> 화면을 구성하기 위한 로직
      - Controller : MVC v1을 가로채서 데이터 작업한후 v2 보냄 MVC는 개념(데이터작업 화면작업 나누자!-> 그럼실제로 어떻게 구현? facade pattern)
        - facade : 문하나로 다 다니자 , c7
        - servelet : controller의 핵심
    - Businesse layer(Service,Application layer) bl+dl => model
      - 통합해서 새로운 걸 만들어냄 
      - 이미 밖에서 만들어져 있는 서비스를 가져다 씀(xml webservice, json restful)
      - SOA(Service Oriented Architecture)
      - interface(Lolipop), DL의 service연결 
    - Data layer : 3개로 나뉨 (ORM)
      - DAO : service가 interface 주면 조립을 함 controller로 보냄 결과를 JSP랑 매핑
      - MyBatis
      - Hibernate
      - 화면이 이동될때 데이터 흐름과 잘 매칭 시키가 Dispatcher pattern (원래 안됨)
  - Engine : request 들어오면 client 요소를 만들어서 response
  - Container (Spring ) 
 - Session 로그인 한사람만 쓸수 있음 Session scope 나만 쓸수잇음 아이디를 Session에 저장 나만 사용할 수 있음
 - requestscope : session scope 이랑 전혀더름 forward
 - JSP 문법 : Scriptlette
 - life cycle이 없는 POJO 객체 끌어 들어감 
 - IOC Inversion Of Controll
 - Framework : Strunts Spring
# File directory
  - src
    - controller
      - LoginServlet
```
	doget()
	doPost()
```
      - LogoutServlet
      - MemberServlet
      - RegisterServlet
    - dao
      - DB.java
      - RegisterDAO.java //interface for RegisterDaoImple
      - MemberService.java
      - RegisterDaoImple.java //sql문 
```
        <form action="./regiAf" method="post">
		<table border="1px">
		...
          	</table>
	</form>
```
    - model
      - member.java //getter, setter, constructer for member
  - WebContent
    - index.jsp
    - main.jsp
    - members.jsp
    - register.jsp //회원가입 기능, form 이용해서 ID, pwd,  
    - login.jsp //로그인기능, form 이용해서 ID pwd 보냄
 - db
  - schema members
    - create table members
      
