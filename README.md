# Getting started with Testcontainers in a Java Spring Boot Project

This is sample code for [Testcontainers in a Java Spring Boot Project](https://christopheranabo.com/post/44-testcontainers-in-a-java-spring-boot-project) Guide.

## 1. Setup Environment
Make sure you have Java 8+ and a [compatible Docker environment](https://www.testcontainers.org/supported_docker_environment/) installed.
If you are going to use Maven build tool then make sure Java 17+ is installed.

For example:

```shell
$ java -version
openjdk version "17.0.4" 2022-07-19
OpenJDK Runtime Environment Temurin-17.0.4+8 (build 17.0.4+8)
OpenJDK 64-Bit Server VM Temurin-17.0.4+8 (build 17.0.4+8, mixed mode, sharing)
$ docker version
...
Server: Docker Desktop 4.12.0 (85629)
 Engine:
  Version:          20.10.17
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.17.11
...
```

## 2. Setup Project

* Clone the repository

```shell
git clone https://github.com/anddegs/test-containers-postgres.git
cd test-containers-postgres
```

* Open the **test-containers-postgres** project in your favorite IDE.

## 3. Run Tests

Run the command to run the tests.

```shell
$ ./mvnw verify  //for Maven
```

The tests should pass.

> [!NOTE]
> The project is configured to automate the code formatting with spotless plugin 
> using prettier-plugin-java, which internally requires Node.js runtime. 
> If you don't have Node.js installed and want to disable the code formatting, 
> you can pass additional parameter to the build command as shown below:

```shell
./gradlew build -x spotlessCheck //for Gradle
./mvnw verify -Dspotless.check.skip=true //for Maven
```
