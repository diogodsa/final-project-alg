# skeleton-spring-boot-single-maven-project
spring-boot, maven, embedded tomcat, web application project



===================



----------


프로젝트 개요
-------------
- maven single project
- spring-boot web application


프로젝트 생성 방법
-------------
1. spring-boot-sample-tomcat-archetype 를 이용해 프로젝트 초기 생성함.

 ```
 ## 콘솔에서 ...
 mvn archetype:generate \
        -DarchetypeGroupId=org.springframework.boot \
        -DarchetypeArtifactId=spring-boot-sample-tomcat-archetype \
        -DgroupId=pe.lygirl \
        -DartifactId=skeleton-spring-boot-single-maven-project \
        -Dversion=0.0.1 \
        -Dpackage=pe.lygirl.skeleton
 ```

2. 1번의 결과로 만들어진 프로젝트 디렉토리 구조

 ```
 >$ cd skeleton-spring-boot-single-maven-project
 >$ tree
 .
 ├── README.md
 ├── pom.xml
 ├── skeleton-spring-boot-single-maven-project.iml
 └── src
     ├── main
     │   ├── java
     │   │   └── pe
     │   │       └── lygirl
     │   │           └── skeleton
     │   │               └── tomcat
     │   │                   ├── SampleTomcatApplication.java
     │   │                   ├── service
     │   │                   │   └── HelloWorldService.java
     │   │                   └── web
     │   │                       └── SampleController.java
     │   └── resources
     │       └── public
     │           └── test.css
     └── test
         └── java
             └── pe
                 └── lygirl
                     └── skeleton
                         └── tomcat
                             ├── NonAutoConfigurationSampleTomcatApplicationTests.java
                             └── SampleTomcatApplicationTests.java
 ```

3. running ...

 ```
 # runnig all test cases
 >$ mvn test

 # running web application
 >$ mvn spring-boot:run
 ```

4.