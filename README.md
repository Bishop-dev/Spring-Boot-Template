**Spring Boot Template**

This project will save your time and health.
The project contains ability to run Spring Boot in Idea and run as *.war file using external Tomcat servlet container.

**How to use it**
1. If you need to run this project in Idea:
- Open `pom.xml` file
- Make sure that following code in dependencies is NOT commented:

        <dependency>
             <groupId>org.springframework.boot</groupId>
             <artifactId>spring-boot-starter-web</artifactId>
         </dependency>
- Make sure that following code is commented:

        <dependency>
             <groupId>org.springframework.boot</groupId>
             <artifactId>spring-boot-starter-tomcat</artifactId>
             <scope>provided</scope>
         </dependency>
- Run project as usual Spring Boot project
            
2. If you need to build project as WAR file to deploy in external Tomcat:
- Open `pom.xml` file
- Make sure that following code in dependencies is commented:

        <dependency>
             <groupId>org.springframework.boot</groupId>
             <artifactId>spring-boot-starter-web</artifactId>
         </dependency>
- Make sure that following code is NOT commented:

        <dependency>
             <groupId>org.springframework.boot</groupId>
             <artifactId>spring-boot-starter-tomcat</artifactId>
             <scope>provided</scope>
         </dependency>
- Run `mvn clean install package`
- Find `*.war` file in `target` folder

**Resources**

This project is a result of 2 other projects merge:

For external Tomcat deployment: https://www.mkyong.com/spring-boot/spring-boot-deploy-war-file-to-tomcat/

For Idea development: https://spring.io/guides/gs/serving-web-content/