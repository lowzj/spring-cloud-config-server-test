# README

```bash
mvn clean package
# start config server
java -Dspring.config.location=configuration/bootstrap.yml -jar config-srver/target/config-server-0.0.1-SNAPSHOT.jar
# start config client
java -jar config-test/target/config-test-0.0.1-SNAPSHOT.jar
```

* config-client的bootstrap.yml里配置的`server.port:9999`
* config-server里的client-test.yml里配置的是`server.port:8999`
* 生效的是 8999
* 在config-client.properties里打开`spring.cloud.config.overrideNone=true`，可以让config-server中的配置优先级最低

另外可参考看下：PropertySourceBootstrapProperties
