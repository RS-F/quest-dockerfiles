# Steps for building a docker'ed application

**Commands used**

- docker-compose up
- ./mvnw spring-boot:build-image -Dspring-boot.build-image.imageName=sea/my-stuff-backend:0.99.2
- find . -name \*\.jar -print
- docker image ls
- docker ps
- docker network ls
- docker run --net quest-dockerfiles_mystuff-net -e SPRING_PROFILES_ACTIVE=docker -p 8080:8080 sea/my-stuff-backend:0.99.2
- docker compose down
- docker volume prune

## git commands

- mkdir quest-dockerfiles
- cd quest-dockerfiles/
- git init
- git remote add origin git@github.com:RS-F/quest-dockerfiles.git
- git add .
- git commit -a
- git push --set-upstream origin master

### Learnings (not working :-( )

- busybox as base not working

- mvn package
- docker build -t my-stuff-backend:0.99.1 .
- docker run --net quest-dockerfiles_mystuff-net -e SPRING_PROFILES_ACTIVE=docker -p 8080:8080 my-stuff-backend:0.99.1
```sh
Exception in thread "main" java.lang.UnsupportedClassVersionError: de/telekom/sea/mystuffbackend/MyStuffBackendApplication has been compiled by a more recent version of the Java Runtime (class file version 55.0), this version of the Java Runtime only recognizes class file versions up to 52.0
```


- docker network ls
- docker run --net quest-dockerfiles_mystuff-net -p 8080:8080 sea/my-stuff-backend:0.99.2
(profile missing)
```sh
com.mysql.cj.jdbc.exceptions.CommunicationsException: Communications link failure
```

