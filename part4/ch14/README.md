# Chapter :one::four: :heavy_minus_sign: Administering and monitoring ActiveMQ

:a: JMX

```
jconsole
```


:b: [Hawt.io](https://hawtio.github.io)



```
wget https://oss.sonatype.org/content/repositories/public/io/hawt/hawtio-app/1.5.11/hawtio-app-1.5.11.jar 
``` 

```
java -jar hawtio-app-1.5.11.jar 
```

<img src="https://github.com/valiha-com/labs/blob/main/images/hawtio-activemq.png" width=304  > </img>


- [ ] ActiveMQ Status

```
${ACTIVEMQ_HOME}/bin/activemq status
```


:warning: `git bash` Terminal has a `ps -o` issue where `status` command is not working

```
ps: unknown option -- o
Try `ps --help' for more information.
ActiveMQ not running
```
As a temporary resolution use:


- [ ] ActiveMQ PID 

```
ps | grep `cat ${ACTIVEMQ_HOME}/data/activemq.pid` 
```


- [ ] Log Files

```
tail -f ${ACTIVEMQ_HOME}/data/activemq.log 
```


# References

- [ ] [Using JMX to monitor Apache ActiveMQ](https://activemq.apache.org/jmx)
- [ ] [How to connect to AMQ JMX using Jconsole remotely](https://access.redhat.com/solutions/252303)
- [ ] [Format 'ps' command output without whitespace](https://unix.stackexchange.com/questions/153157/format-ps-command-output-without-whitespace)
