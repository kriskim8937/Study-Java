## Dependency_Injection

## What is?
- 소프트웨어 공학에서 dependency injection은 하나의 object가 다른 object에게 depnency를 제공하는 기술이다.
- dependency란 예를 들어 service로 써 사용 될 수 있는 object이다.
- client가 어떤 service를 사용하는지를 명시하는 대신, 어떤 다른 것이 client에게 어떤 service를 사용해야 되는지 말해준다. 
- injection이란 depndency(a service)를 object(client) 안으로 집어 넣는 것을 말한다.
- service는 client의 state의 일부로 만들어진다. 
- 이 패턴의 기본은, client가 service를 찾거나 build 하는 대신 service를 client로 넘겨주는데 있다.
- dependency injection의 의도는 object에 대한 construction과 use에대해서 separation of concern을 성취하는 것이다. 이것은 가독성과 코드 재사용성을 증대 시킨다.
- dependency injection is a technique whereby one object supplies the dependencies of another object
- Dependency injection is one form of the broader technique of inversion of control.
- This means the client does not need to know about the injector, how to construct the services, or even which actual services it is using.
- The client only needs to know about the intrinsic interfaces of the services because these define how the client may use the services. 
- This separates the responsibility of "use" from the responsibility of "construction".
## Why?
- Dependency Injection solves problems such as
  - How can an application or class be independent of how its objects are created?
  - How can the way objects are created be specified in separate configuration files?
  - How can an application support different configurations?


