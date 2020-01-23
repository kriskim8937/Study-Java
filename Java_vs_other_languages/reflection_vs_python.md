dynamic class loading
	- 동적 클래스 로딩은 프로그램 시작전에 알려지지 않은 자바 코드를 로드할 수 있게 해준다.
	- 이말은 , compile이 완료 되지 않고? dependency가 전부 연결되지 않은 class를 load 할 수 있따는 말이다. 
	- compile time에 load 되지 않고, run time에 load 된다?


자바 키워드

	- 동적 로딩 , reflection , 정적 로딩, 런타임 로딩, 
	- compile time runtime
	- Jvm 의 작동 방식 
	- delegation model

## usage for reflection:

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
