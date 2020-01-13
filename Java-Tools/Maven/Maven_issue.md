## Maven_issue
- dependency conflict
  - NullPointerException 이나 NoSuchMethodExcepthion등이 발생할 수 있음
  - 해결 프로세스 :
    - dependency를 가장 최신버전으로 업그레이드
    - library code를 살표보기, method나 class가 아예 없다는 것을 발견!
   - dependency들이 서로다른 version의 같은 dependency에 의존할 수 있음... 이걸 어떻게 해결?
 - Transitive Dependencies 
  > 내가 manual하게 지정한 dependency가 의존하는 내가 지정하지 않은 dependency들!
  - dependency mechanism
    - dependency tree 구조에서 root, 즉 내가 pom파일에 지정한 dependency와 가장 가까운 dependency가 우선적으로 쓰임 
    - 동일한 level에 여러개의 dependency가 있을 경우 첫 번째로 발견된 라이브러리가 쓰임 이말은 pom파일에 dependency순서에 따라 뭘쓸지 결정된다는 말
  - How to solve conflict
    - 충돌이 나는 라이브러리를 pom파일에 직접 먼저 설정함


## references
- https://dzone.com/articles/solving-dependency-conflicts-in-maven
