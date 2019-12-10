## Maven

## What is maven?
> Maven, a [Yiddish word](https://en.wikipedia.org/wiki/Maven) meaning *accumulator of knowledge*, began as an attempt to simplify the build processes in the Jakarta Turbine project. There were several projects, each with their own Ant build files, that were all slightly different. JARs were checked into CVS. We wanted a standard way to build the projects, a clear definition of what the project consisted of, an easy way to publish project information and a way to share JARs across several projects.
The result is a tool that can now be used for building and managing any Java-based project. We hope that we have created something that will make the day-to-day work of Java developers easier and generally help with the comprehension of any Java-based project.

## Object of Maven
- Making the build process easy
- Providing a uniform build system
- Providing quality project information
- Providing guidelines for best practices development
- Allowing transparent migration to new features

## 1. Making the build process easy
While using Maven doesn’t eliminate the need to know about the underlying mechanisms, Maven does provide a lot of shielding from the details.

## 2. Providing a uniform build system
Maven allows a project to build using its project object model (POM) and a set of plugins that are shared by all projects using Maven, providing a uniform build system. Once you familiarize yourself with how one Maven project builds you automatically know how all Maven projects build saving you immense amounts of time when trying to navigate many projects.

## 3. Providing quality project information
Maven provides plenty of useful project information that is in part taken from your POM and in part generated from your project’s sources. For example, Maven can provide:

- Change log document created directly from source control
- Cross referenced sources
- List of mailing lists managed by the project
- Dependency list
- Unit test reports including coverage
As Maven improves the information set provided will improve, all of which will be transparent to users of Maven.

Other products can also provide Maven plugins to allow their set of project information alongside some of the standard information given by Maven, all still based on the POM.

## 4. Providing guidelines for best practices development
Maven aims to gather current principles for best practices development, and make it easy to guide a project in that direction.

For example, specification, execution, and reporting of unit tests are part of the normal build cycle using Maven. Current unit testing best practices were used as guidelines:

- Keeping test source code in a separate, but parallel source tree
- Using test case naming conventions to locate and execute tests
- Having test cases setup their environment instead of relying on customizing the build for test preparation
Maven also aims to assist in project workflow such as release and issue management.

Maven also suggests some guidelines on how to layout your project’s directory structure. Once you learn the layout you can easily navigate any other project that uses Maven and the same defaults.

## Allowing transparent migration to new features
Maven provides an easy way for Maven clients to update their installations so that they can take advantage of any changes that have been made to Maven itself.

Installation of new or updated plugins from third parties or Maven itself has been made trivial for this reason.

## What is Maven Not?
You may have heard some of the following things about Maven:

- Maven is a site and documentation tool
- Maven extends Ant to let you download dependencies
- Maven is a set of reusable Ant scriptlets
While Maven does these things, as you can read above in the “What is Maven?” section, these are not the only features Maven has, and its objectives are quite different.

Maven does encourage best practices, but we realise that some projects may not fit with these ideals for historical reasons. While Maven is designed to be flexible, to an extent, in these situations and to the needs of different projects, it can not cater to every situation without making compromises to the integrity of its objectives.

If you decide to use Maven and have an unusual build structure that you cannot reorganise, you may have to forgo some features or the use of Maven altogether.

## Feature Summary
The following are the key features of Maven in a nutshell:

- Simple project setup that follows best practices - get a new project or module started in seconds
- Consistent usage across all projects - means no ramp up time for new developers coming onto a project
- Superior dependency management including automatic updating, dependency closures (also known as transitive dependencies)
- Able to easily work with multiple projects at the same time
- A large and growing repository of libraries and metadata to use out of the box, and arrangements in place with the largest Open Source projects for real-time availability of their latest releases
- Extensible, with the ability to easily write plugins in Java or scripting languages
- Instant access to new features with little or no extra configuration
- Ant tasks for dependency management and deployment outside of Maven
- Model based builds: Maven is able to build any number of projects into predefined output types such as a JAR, WAR, or distribution based on metadata about the project, without the need to do any scripting in most cases.
- Coherent site of project information: Using the same metadata as for the build process, Maven is able to generate a web site or PDF including any documentation you care to add, and adds to that standard reports about the state of development of the project. Examples of this information can be seen at the bottom of the left-hand navigation of this site under the "Project Information" and "Project Reports" submenus.
- Release management and distribution publication: Without much additional configuration, Maven will integrate with your source control system (such as Subversion or Git) and manage the release of a project based on a certain tag. It can also publish this to a distribution location for use by other projects. Maven is able to publish individual outputs such as a JAR, an archive including other dependencies and documentation, or as a source distribution.
- Dependency management: Maven encourages the use of a central repository of JARs and other dependencies. Maven comes with a mechanism that your project's clients can use to download any JARs required for building your project from a central JAR repository much like Perl's CPAN. This allows users of Maven to reuse JARs across projects and encourages communication between projects to ensure that backward compatibility issues are dealt with.

## 메이븐
- build tool이다! ANT가 단지 build tool 에 가까웠다면 Maven은 훨씬 다양한 기능을 제공한다.
- build too로써의 역할 -> src, resource를 통해서 jar, war 파일을 생성한다. (Ant도 같은 기능이 가능하다)
- 표준 디렉토리 구조를 가짐으로써, 메이븐을 이용하는 누구나 파일 디렉토리를 쉽게 이해하고, 어떠한 디렉토리를 따로 설정할 필요가 없다.
- dependency management, 메이븐 통합 레포지토리를 통해서 쉽게 라이브러리를 연결하고 업그레이드 할 수 있다.
- 표준 인터페이스를 제공한다. mvn install 만으로 build가 가능하다.
## Key words
- life cycle : life cycle은 phase의 집합이다 default는 validate, compile, test, package, integration-test, verify, install, deploy이다
- phase : 페이즈는 빌드 라이프사이클에서 순서만을 정의하고 있는 개념으로 직접 작업을 하는 것은 아니다. 직접 작업하는것은 plug in
- site : site document? 프로젝트 문서
- plug in : 메이븐의 모든 작업은 플러그인 기반으로 동작한다. 
- goal : 한 plug in은 여러가지 goal을 실행할 수 있다. 

## life cycle
- validate
- compile : 코드를 기계어로, 즉 java파일을 class로 변환하는 과정
- test
- package
- integration-test
- verify
- install
- depoy
