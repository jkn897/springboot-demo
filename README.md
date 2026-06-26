# Spring REST Hello World Example

Article link : https://www.mkyong.com/spring-boot/spring-rest-hello-world-example/

## 1. How to start
```
$ git clone https://github.com/mkyong/spring-boot.git
$ cd spring-rest-hello-world
$ mvn spring-boot:run

$ curl -v localhost:8080/books
```

### Send app logs directly to kibana (Not related with above)
1. Download ELK , do all setup and it(elastic & kibana) must be up and running.  
2. Place the logback-spring.xml file which is available in the root directory in src/main/resources path.  
3. Start the spring boot app and hit the available end points for log printing.   
**Note**:  
This is already tested with below tech
jdk11 , spring-boot 2.7.13 and elk elasticsearch-8.12.2

### Steps to view the logs in kibana
1. Find the index name mentioned in previous step logback-spring.xml file.  
2. Go to kibana ui and in index section check it's availability, if the same index is available then discover it to view the logs.  

This is tried using the below url and it worked.
https://thirumurthi.hashnode.dev/ship-springboot-app-logs-directly-to-elastic-search
