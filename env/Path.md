## Path

### 1. Java path
- Java를 운영체제 상에서 실행시키기 위한 JDK binaries를 찾기 위한 경로
- PATH is an environment variable which is used to locate JDK binaries like "java" or "javac" command used to run java program and compile java source file. 
- In order to set PATH in Java, you need to include JDK_HOME/bin directory in PATH environment variable 
- Another significant difference between PATH and CLASSPATH is that PATH can not be overridden by any Java settings but CLASSPATH can be overridden by providing command line option -classpath or -cp to both "java" and "javac" commands or by using Class-Path attribute in Manifest file inside JAR archive.
- PATH environment variable is used by operating system to find any binary or command typed in the shell, this is true for both Windows and Linux environment while CLASSPATH is only used by Java ClassLoaders to load class files.
### 2. Class path
- 클래스를 찾기 위한 경로
- On the other hand, CLASSPATH, an environment variable is used by System or Application ClassLoader to locate and load compile Java bytecodes stored in the .class file.
- In order to set CLASSPATH in Java you need to include all those directories where you have put either your .class file or JAR file which is required by your Java application.
- JVM이 프로그램을 실행 할 때 클래스 파일을 찾는데 기준이 되는 경로
- Java runtime(java 또는 jre)가  .class 파일에 포함된 명령을 실행하려면 이 파일을 찾아야한다.
#### classpath 지정 하는 방법
- 환경변수 class path사용
- Java runtime에 -classpth 플래그를 사용하는 방법
