## Maven Tutorial
### Creating a Project
- Maven Goal에 파라미터들을 주어서 실행시킨다! Plugin은 같은 목표를 가진 goal들의 집합이다. 
> mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
### Build tha Project
- Phase를 작동시킨다. Phase는 build lifecycle의 step 중 하나이다. Phase를 작동시키면 그 페이즈를 포함한 이전 페이즈 까지 실행된다.
> mvn package
## Maven command
- mvn --version


## Build-Cycle
- validate - validate the project is correct and all necessary information is available
- compile - compile the source code of the project
- test - test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed
- package - take the compiled code and package it in its distributable format, such as a JAR.
- verify - run any checks on results of integration tests to ensure quality criteria are met
- install - install the package into the local repository, for use as a dependency in other projects locally
- deploy - done in the build environment, copies the final package to the remote repository for sharing with other developers and projects.
