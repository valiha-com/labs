# Chapter :three:


- [ ] Open [VSC](https://code.visualstudio.com)

```
code .
```

- [ ] 2 coding examples

| component | Source Code |  Schematic |
|-----------|-------------|--|
| Queue     | [jobs](src/main/java/org/apache/activemq/book/ch3/jobs) | <img src="../../images/job-queue-example.png" width=517 height=231  /> </img> |
| Topic     | [portfolio](src/main/java/org/apache/activemq/book/ch3/portfolio) | <img src="../../images/stock-portfolio-example.png" width=528 height=237  /> </img> |

# [:back: ](..) Return to Part:one:

# References

- [ ] External `Maven` Libraries used for this chapter

| Maven Libraries                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|
| [javax.jms/javax.jms-api/2.0.1](https://mvnrepository.com/artifact/javax.jms/javax.jms-api/2.0.1)                     |
| [org.apache.activemq/activemq-all/5.16.2](https://mvnrepository.com/artifact/org.apache.activemq/activemq-all/5.16.2) |

- [ ] :steam_locomotive: Running the app using `java` binary

:bulb: observe the `-classpath` argument which is extra long

```
java \
-classpath target/ch3-1.0-SNAPSHOT.jar:$HOME/.m2/repository/javax/jms/javax.jms-api/2.0.1/javax.jms-api-2.0.1.jar:$HOME/.m2/repository/org/apache/activemq/activemq-all/5.16.2/activemq-all-5.16.2.jar \
org.apache.activemq.book.ch3.jobs.Producer 
```

