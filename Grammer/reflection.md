## Summary
- 리플렉션이 가진 기능들
- 활용 방안
	- annotation
- 어떻게 이게 가능한지
- 다른 언어에 있는 기능과의 

## What is ?
  - process to examine, introspect, and modify its own structrue and behavior.
  - 클래스의 구조를 개발자가 확인하고, 값을 가져오거나 메소드를 호출할 때사용
  
## Where to use?
- Spring Framework
  - 런타임 시에 개발자가 등록한 빈을 애플리케이션에서 가져와 사용가능
- ORM Hibernate
- Jackson library
- 

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
자바 키워드

	- 동적 로딩 , reflection , 정적 로딩, 런타임 로딩, 
	- compile time runtime
	- Jvm 의 작동 방식 
	- delegation model

## 리플렉션의 장점
- 구체적인 클래스 타입을 알지 못해도, 그 클래스의 메소드, 타입, 변수들을 접근할 수 있게 해주는 자바 api
	- object 라는 타입으로, 어떠한 클래스의 인스턴스든 담을 수 있지만, 사용 가능한 메소드는 object에 정의된 메소드와 변수들 뿐..
- 내가 만드는 프로그램의 코드 흐름인데, 내가 사용할 클래스의 이름과 타입을 모르는 경우가 있나????
	- compile타임에 어떤 타입의 클래스를 사용할지 모르는 경우가 있다! 이럴 때는 runtime에 클래스를 가져와서 실행해야한다.
	- 대표적으로 프레임 워크나 IDE에서 이러한 동적 바인딩을 이용한 기능을 제공한다.
	- annotaion, intellij의 자동 완성등이 설계할 때는 사용될 클래스가 어떤 타입인지 모르지만 리플렉션을 이용해서 코드를 일단 작성하고 실행할 시점에 활용하게 해줌
	- Reflection은 구체적은 클래스 타입을 알지 못해도, 클래스의 메소드, 타입 변수들을 접근할 수 있도록 해주는 JAVA API

- 어떻게 이게 

## usage for reflection:
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
...


JVM  내부 구조
	- Class Loader subsystem
		○ feature of class Loader
			§ Hierarchical
			§ Delegate load request 
				□ delegation은 class Loader을 이해하는데 매우 중요한 역할을 한다. 
			§ Have Visibility Constraint
			§ Cannot unload classes
	- Runtime data area
		○ Method area
		○ Heap
		○ Java satck
		○ Pc register
		○ Native Method stack
	- Excecution engine



Class Loader 

자바 코드 실행 
	- 자바는 compile time과 run time으로 나뉘어져서 실행된다.
		○ JVM위에서 실행되기 때문에 다양한 플랫폼 환경에서도 실행가능하다. 
	- compile time
		○ source code를 byte code로 변환한다.
	- run time
		○ byte code가 JVM(Java Virtual Machine)위에서 실행된다.
			§ 이때 machine 코드로 변환되는 부분도 있고, interprete 되는 부분도 있다. 
	- references
		○ https://stackoverflow.com/questions/846103/runtime-vs-compile-time


jar 파일로 배포. 
exe , exutable 한 파일로 배포 



JAVA에서는 모든 object들이 Heap 메모리에 할당된다. 
그와 다르게, c++ 에서는 object 들이 Stack , Heap 둘다 할당 될 수 있다. 
C++ 에서는 , new () 를 사용해서 객체를 할당할 때, object가 Heap에 할당되고,
global이나 static 이 아닌 다른 object들은 stack 에 할당된다. 

자바에서는 class type의 variable을 선언했을때 오직 reference만 생성된다. 
(이때memory가 object에 할당되지 않는다.)  
object에 메모리를 할당하기 위해서는 new()를 사용해야만한다.  
그 때문에, object는 항상 heap memory를 할당 받는다. 

heap이 꽉차면, garabage 가 collect 된다. 



Python Decorator vs Java Annotation
	- 

Python __dict__ vs Java reflection 
	-  공통점 :
		○ 둘다 introspection, class 내부를 탐색하는 것이 목표이다.
		○ pascal, c, c++ 에는 이러한 기능이 없다. 
	- Java reflection 
		○ introspect 뿐만 아니라 내부를 조작할 수도 있다. 
		○ class 내부의 멤버를 전부 보여줄 수 있따. 
		
	- Python dict: 
		○ 파이썬 class body안에 어떤 attribute들이 정의되어 있는지 보여주는 기능을 한다.
주의할 점 : __dict__는 class가 difinition syntax를 사용하고, 이 class가 만들어진 직후에만 신뢰성(reliablility)을 가진다. 
