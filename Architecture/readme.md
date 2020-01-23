## Java Architecture

### 1. class

### 2. package

### 3. module
- JAVA 9 부터 도입된 개념이다. 
- 이전까지 패키지는 다른 패키지의 public method만 접근이 가능했다. 
- 커다란 코드를 다룰때 다른 패키지의 모든 public method에 접근이 가능하다는 것은 문제이다.
- module을 사용해서 package들의 public method간의 accessibility를 조절할 수 있게 되었다.
- module은 패키지의 집합이다. package의 public method들은 같은 module 안에 있는 package 끼리만 접근 가능하다.

###
- JVM architecture
- JRE architecture


### references
- https://www.concretepage.com/java/java-9/java-module
