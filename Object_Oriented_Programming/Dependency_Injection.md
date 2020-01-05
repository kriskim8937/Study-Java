## Dependency_Injection

## What is?
- 소프트웨어 공학에서 dependency injection은 하나의 object가 다른 object에게 depnency를 제공하는 기술이다.
- dependency란 예를 들어 service로 써 사용 될 수 있는 object이다.
  - service란 ? client와 service 관계로 특정 protocol에 따라 client가 요청한 정보를 service가 제공해 주는것 
- client가 어떤 service를 사용하는지를 명시하는 대신, 어떤 다른 것이 client에게 어떤 service를 사용해야 되는지 말해준다. 
- injection이란 depndency(a service)를 object(client) 안으로 집어 넣는 것을 말한다.
- service는 client의 state의 일부로 만들어진다. 
- 이 패턴의 기본은, client가 service를 찾거나 build 하는 대신 service를 client로 넘겨주는데 있다.
- dependency injection의 의도는 object에 대한 construction과 use에대해서 separation of concern을 성취하는 것이다. 이것은 가독성과 코드 재사용성을 증대 시킨다.
- dependency intection은 inversion of control의 기술중 하나이다.
- service를 호출하는 client는 service를 어떻게 구성하는지 알 필요가 없다. 
- 예시) 니가 사업을 해, 각 분야 전문가들을 다 고용 할꺼야? 아니면 그 분야 회사들과 계약해서 service를 가져다 쓸거야??
- 만약 후자라면, 장소도 필요없고, 사업을 키우거나 줄일때 그에 맞는 회사로 바꿀 수도 있지! 그 분야에 대해서 알필요가 없어져

## Why?
- Dependency Injection solves problems such as
  - How can an application or class be independent of how its objects are created?
  - How can the way objects are created be specified in separate configuration files?
  - How can an application support different configurations?


