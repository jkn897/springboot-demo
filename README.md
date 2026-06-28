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

### Send app logs directly to kibana using logstash (Not related with above)
1. After starting elastic, start logstash using the logstash.conf file exist in the root directory. 
   **bin>logstash -f D:\Downloads\extract\logstash-8.12.2\config\logstash.conf**
2. If logstash is started then add "logstash-logback-encoder" dependency in the spring boot app pom file.  
3. Then add the logback-spring(logstash) in src/main/resources path which is available in the root directory.
4. Then start the app and hit available endpoints.
5. Go to kibana and verify the logs
**Note**
Tested already and used the below link
https://betterstack.com/community/questions/send-spring-boot-logs-directly-to-logstash-with-no-file/
