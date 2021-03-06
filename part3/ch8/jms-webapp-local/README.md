# :cat2: Tomcat


## :a: Create a `war` (web archive) file 

- [ ] Open a terminal window and position yourself into the `jms-webapp-local` working directory

```
cd ${LABS}/part3/ch8/jms-webapp-local
```

- [ ] Open [VSC](https://code.visualstudio.com)

```
code .
```

- [ ] Generate the war file 

```
mvn package
```

## :b: Create the application server running in Docker

- [ ] Generate the image using the preconfigured [`Dockerfile`](Dockerfile)


```
docker build --tag labs/tomcat-8:8.5.79 . 
```

- [ ] Check that the `labs/tomcat-8:8.5.79` image was generated

```
docker image ls
```

- [ ] Run the newly generated image

* The new container will appear on port `8088`

```
docker container run --name some-tomcat --publish 8088:8080 --detach labs/tomcat-8:8.5.79
```

- [ ] Visit the `SampleWebApp` App Server

http://localhost:8088/jms-webapp/send.html

:warning: When pressing `send` a `Java` stacktrace will appear

As an exercice, the XML configuration file can be tuned to make the broker working properly


## :x: Clear your image from the repositories

- [ ] When your tests are done `forcibly` remove the container

```
docker container rm -f some-tomcat
```

- [ ] clear the image
 
```
docker image rm labs/tomcat-8:8.5.79
```

# [:back: ](..) Return to ch:eight:

# References

- [ ] [Docker Tomcat Example – Dockerfile for Tomcat, Docker Tomcat Image](https://www.middlewareinventory.com/blog/docker-tomcat-example-dockerfile-sample)
- [ ] [Getting java.lang.ClassNotFoundException: org.springframework.web.servlet.mvc.annotation.AnnotationMethodHandlerAdapter](https://stackoverflow.com/questions/56684075/getting-java-lang-classnotfoundexception-org-springframework-web-servlet-mvc-an)
- [ ] [mvc:annotation-driven is not bound](https://stackoverflow.com/questions/6001593/mvcannotation-driven-is-not-bound)
