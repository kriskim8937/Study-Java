## What is ?
- In object-oriented programming languages such as Java, reflection allows inspection of classes, interfaces, fields and methods at runtime without knowing the names of the interfaces, fields, methods at compile time. It also allows instantiation of new objects and invocation of methods. 
- process to examine, introspect, and modify its own structrue and behavior.
- 클래스의 구조를 개발자가 확인하고, 값을 가져오거나 메소드를 호출할 때사용
- 컴파일 타임에 클래스의 type을 몰라도 Object로 선언하고 내부의 값을 확인하고 수정할 수 있음
- 구체적인 클래스 타입을 알지 못해도, 그 클래스의 메소드, 타입, 변수들을 접근할 수 있게 해주는 자바 api
	- 자바에서는 기본적으로 object 타입에 어떠한 클래스의 인스턴스든 담을 수 있지만, 사용 가능한 메소드는 object에 정의된 메소드와 변수들 뿐..
- 내가 만드는 프로그램의 코드 흐름인데, 내가 사용할 클래스의 이름과 타입을 모르는 경우가 있나????
	- compile타임에 어떤 타입의 클래스를 사용할지 모르는 경우가 있다! 이럴 때는 runtime에 클래스를 가져와서 실행해야한다.
	- 대표적으로 프레임 워크나 IDE에서 이러한 동적 바인딩을 이용한 기능을 제공한다.
	- annotaion, intellij의 자동 완성등이 설계할 때는 사용될 클래스가 어떤 타입인지 모르지만 리플렉션을 이용해서 코드를 일단 작성하고 실행할 시점에 활용하게 해줌
	- Reflection은 구체적은 클래스 타입을 알지 못해도, 클래스의 메소드, 타입 변수들을 접근할 수 있도록 해주는 JAVA API
  
## Where to use?
- Reflection helps programmers make generic software libraries to display data, process different formats of data, perform serialization or deserialization of data for communication, or do bundling and unbundling of data for containers or bursts of communication. 
- Effective use of reflection almost always requires a plan: A design framework, encoding description, object library, a map of a database or entity relations. 
- Reflection makes a language more suited to network-oriented code. 
- Reflection can be used for observing and modifying program execution at runtime.
- Reflection is often used as part of software testing, such as for the runtime creation/instantiation of mock objects. 
- Reflection is also a key strategy for metaprogramming. 
- In some object-oriented programming languages, such as C# and Java, reflection can be used to bypass member accessibility rules
#### use cases
- Spring Framework
  - 런타임 시에 개발자가 등록한 빈을 애플리케이션에서 가져와 사용가능
- ORM Hibernate
- Jackson library
- Access private fields, violation of the objec oriented concept
- Late binding
- Security (introspect code for security reasons)
- Code analysis
- Dynamic typing (duck typing is not possible without reflection)
- Metaprogramming
- Developed plugin system based on reflection
- Used aspect-oriented programming model
- Performed static code analysis
- Used various Dependency Injection frameworks

## How to use?
- class.getSuperClass()
  - return super class
- class.getClass()
  - 상속된 클래스를 포함하여 모든 공용 클래스, 인터페이스, 열거형 반환
- class.getDeclaringClass() 
  - 클래스에 명시적으로 선언된 클래스 반환
- class.getEnclosingClass()
  - 클래스에 enclose된 클래스 반환
dynamic class loading
- 동적 클래스 로딩은 프로그램 시작전에 알려지지 않은 자바 코드를 로드할 수 있게 해준다.
- 이말은 , compile이 완료 되지 않고? dependency가 전부 연결되지 않은 class를 load 할 수 있다는 말이다. 
- compile time에 load 되지 않고, run time에 load 된다?


## How is it works?
- java 언어는 compile시에 바로 machine code로 번역되는 것이 아니라 byte 코드로 변형 되고 runtime에 machine code로 번역되기에 가능하다.
- compile 타임에 번역되더라도 runtime에는 
자바 키워드

	- 동적 로딩 , reflection , 정적 로딩, 런타임 로딩, 
	- compile time runtime
	- Jvm 의 작동 방식 
	- delegation model

## Pros and Cons
#### Pros
- Reflection makes a language more suited to network-oriented code. 
	- it assists languages such as Java to operate well in networks by enabling libraries for serialization, bundling and varying data formats.
	- Languages without reflection (e.g. C) have to use auxiliary compilers, e.g. for Abstract Syntax Notation, to produce code for serialization and bundling. 
		- Abstract Syntax Notaion : 여기서 ASN.1이 나오네, 카이 인공위성 소프트웨어에서 이거 씀 우리도 쓴다했던 것 같은데 

## reference
- https://en.wikipedia.org/wiki/Reflection_(computer_programming)#Java 
	- 각언어에서 reflection 사용 예
	- reflectino의 장점, 어디에 쓰이는지


