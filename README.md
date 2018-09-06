### SCDF 学习笔记
> [SCDF官方文档](http://docs.spring.io/spring-cloud-dataflow/docs/1.7.0.BUILD-SNAPSHOT/reference/htmlsingle/#getting-started)

--------------------


##### 1. 注册APP
* 1.1 http://docs.spring.io/spring-cloud-dataflow/docs/1.7.0.BUILD-SNAPSHOT/reference/htmlsingle/#spring-cloud-dataflow-register-stream-apps
* 1.2. app import --uri http://bit.ly/Darwin-GA-stream-applications-kafka-10-maven
* 1.3. app import --uri http://bit.ly/Darwin-GA-stream-applications-rabbit-maven
* 1.4. app register --name task1 --type task --uri maven://com.example:mytask:1.0.2
* 1.5. app register --name task2 --type task --uri file:///Users/example/mytask-1.0.2.jar
* 1.6. app register --name task3 --type task --uri http://example.com/mytask-1.0.2.jar
* 1.7. echo "task.foo=file:///tmp/foo.jar\r\ntask.bar=file:///tmp/bar.jar" > /tmp/task-apps.properties & app import --uri /tmp/task-apps.properties

##### 2. 查看APP的属性
> eg: 
* app info --id task:timestamp
* app info --name timestamp --type task

##### 3. 查看APP的属性
> 查看正在运行的APP，以及APP的log路径
`runtime app`


