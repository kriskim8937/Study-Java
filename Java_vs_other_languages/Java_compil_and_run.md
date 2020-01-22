## Comparison_with_other_language

### How it works?
- 자바는 compile 언어와 interprete언어중에 무엇일까?
- 컴파일 언어는 source code를 compile과정을 통해 bytecode(machine code와 다르다! virtual machine에 의해 실행된다.)로 변환하는 언어이다.
- interprete언어는?
- Machine code는 cpu에서 바로 실행가능한, 이진수로된 명령어이다.
- 자바는 javac에 의해서 compile되어 javac코드로 변환된다. 이때까지가 Compile-time Environment다! 
- 이러한 java byte코드는 JVM에서 실행된다. JVM은 JIT compilation이라는 기술을 사용하여 byte code를 machine code로 변환한다.
- 어떠한 부분은 Java 에 의해 interprete된다. Python같은 경우는 바로 interprete하지만 이건 byte code를 interprete 함으로 다르다.
- 그리고는 JIT Compiler가 이를 machine코드로 변환시키거나, Java interpreter가 이를 interpret한다. 
- 환경에 따라서 java byte코드는 다음 4가지가 가능하다
  - compiled ahead of time and executed as native code (similar to most C++ compilers)
  - compiled just-in-time and executed
  - interpreted
  - directly executed by a supported processor (bytecode is the native instruction set of some CPUs)
### Why interpreter?
- platform independency
- Security of program from virus
