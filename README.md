# Steps for building a docker'ed application

**Commands used**

- ./mvnw spring-boot:build-image -Dspring-boot.build-image.imageName=sea/my-stuff-backend:0.99
- find . -name \*\.jar -print
- docker build -t sea/my-stuff-backend:0.99 .
- docker image ls


## git commands

- mkdir quest-dockerfiles
- cd quest-dockerfiles/
- git init
- git remote add origin git@github.com:RS-F/quest-dockerfiles.git
- git add .
- git commit -a
- git push --set-upstream origin master

### Learnings

- busybox as base not working
- mvnw package throws exception:
```sh
Exception in thread "main" java.lang.UnsupportedClassVersionError: de/telekom/sea/mystuffbackend/MyStuffBackendApplication has been compiled by a more recent version of the Java Runtime (class file version 55.0), this version of the Java Runtime only recognizes class file versions up to 52.0
```

