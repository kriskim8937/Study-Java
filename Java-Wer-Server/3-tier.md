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
 
# MVC를 구현하기 위한 3대 패턴
Model
-dao 
view
- jsp 가 뷰맡음
controller
-servelet 을 이용해서 흐름제어, 나중에는 controller 라는 클래스가 나옴 
FACADe 패턴
service 는 Singletone 패턴
Dao는 Factory 패턴
Dispatcher 패턴
servelet scope 란 객체 
서블릿에서 내장객체가 들어옴 걔네 수명 이 스코프
리퀘스트 객체는 클라이언트가 뭔가 받이면 사라짐
포워드는 서블릿에서 서블릿 리스폰스 리퀘스트 같이 보냄 
세션은 리퀘스트가 계속 바뀌어도 세션이 살아있음 쿠키 베이스 랜덤 난수를 쿠키로 발급하고 그걸로 판별
ajax는 톰캣은 가고 html은 남겨두고  html 사이드에서 request 없음 응답이 http로 안오고 데이터가 안옴 

https://www.javajee.com/application-request-session-and-page-scopes-in-servlets-and-jsps
- 화명에서만 객체 쓰고 끝남 페이즈 스코프
- forward하면 계속 객체 전달가능 주고받은 곳에만 있음 아니면 없어짐 request scope
- 내꺼는 어딜가든 '나만' 마음대로 사용할 수 있음 session scope
- 누구나 가져다 쓸수 있는 영역 applicaiton scope

- jsp 기본, 내장 객체
- jsp는 이미 servlet 될 준비가 되어 있음
- 서버는 상대경로를 못찾음 절대 경로 ,request parameter
- 서버에서 클라이언트는 response 

# 쿠키 
- 접속 기록 남기기
- 컴퓨터에 심어놈
- 쿠키 모으는 사기꾼 hooker

# Page 디렉티브
https://hyeonstorage.tistory.com/73

# include
https://fruitdev.tistory.com/88
- 정적인클루드
- 동적 인클루드

# JSTL
- JSTL 이란? https://mkil.tistory.com/249
- taglib로 사용가능


# File directory
  - src
    - controller
      - LoginServlet
      - LogoutServlet
      - MemberServlet
      - RegiCheck
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
      
