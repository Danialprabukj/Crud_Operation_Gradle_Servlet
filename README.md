gradle init

```
plugins {
	id 'org.gretty' version '3.0.9'
    id 'com.github.johnrengelman.shadow' version '7.0.0'

}

apply plugin: 'java'
apply plugin: 'war'
apply plugin: 'idea'

// JDK for your java version
sourceCompatibility = 1.8
targetCompatibility = 1.8

repositories {
    mavenCentral()
}

dependencies {
    implementation 'mysql:mysql-connector-java:8.0.33'
    compileOnly 'jakarta.servlet:jakarta.servlet-api:6.0.0'
    implementation 'com.google.code.gson:gson:2.9.0'

}



gretty {
	httpPort = 8080
	contextPath = '/'
	//servletContainer = 'jetty9.4'
	servletContainer = 'tomcat9'
}
```

gradle clean  - Clean the project
gradle build   -  Build the project
gradle tomcatRunWar   -  Run the web application
gradle dependencies --configuration compileClasspath
Ctrl+Shift+P(Command Pallete) -> Clean Java server language workspace-> Restart and delete. - If your intellisense is not working, follow this step to fix the error.



https://mkyong.com/spring-mvc/gradle-spring-mvc-web-project-example/

https://stackoverflow.com/questions/67680483/getting-error-file-cannot-be-resolved-to-a-type-for-java-in-visual-studio-code