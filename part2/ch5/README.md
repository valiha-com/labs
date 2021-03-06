# Chapter :five: :heavy_minus_sign: ActiveMQ message storage 


:gear: [Docker](https://www.docker.com/)

:bulb: This activity needs :whale2: Docker Desktop, make sure it is running.

- [ ] Open [VSC](https://code.visualstudio.com)

```
code .
```

- [ ] Add the `MySQL Connector/J » 8.0.29` Library to the project management file `pom.xml`

- [ ] Add the `mysql` database jar file to the broker's library folder by using the below copy command.

```
cp ${HOME}/.m2/repository/mysql/mysql-connector-java/8.0.29/mysql-connector-java-8.0.29.jar ${ACTIVEMQ_HOME}/lib
```



| Source  |  Storage Type | Available |
|---------|--|----|
| [jdbc](jdbc) |  JDBC Persistence | :heavy_check_mark: |


# References

- [ ] External `Maven` Libraries used for this chapter

| Maven Libraries                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|
| [MySQL Connector/J » 8.0.29](https://mvnrepository.com/artifact/mysql/mysql-connector-java/8.0.29)                     |

- [ ] [ActiveMQ - Persistence](http://activemq.apache.org/persistence.html)
- [ ] [AMQ Message Store](https://activemq.apache.org/amq-message-store)
