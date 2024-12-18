# Task1-SpringBoot

## Task Description
The goal of this task was to create a simple application using the **Spring Boot** framework. The application includes a controller that handles HTTP GET requests and returns a simple response. Due to a system conflict, the default port has been changed from `8080` to `8081`.

## Application Features
1. **Controller** – handles HTTP GET requests on the root path (`/`) and returns a text message.
2. **Port Configuration** – the application runs on port `8081` instead of the default `8080`.
3. **Simple Response** – the application returns the message:
   ```
   Hello Vistula, in my first Spring controller.
   ```

## Port Configuration
The port was changed by adding the following configuration to the `application.properties` file:

```properties
server.port=8081
spring.application.name=Task1
```

## Project Structure
The following is the directory structure of the application:

```
src
├── main
│   ├── java
│   │   └── com
│   │       └── AL_VIS
│   │           └── Task1
│   │               ├── Task1Application.java        # Main application class
│   │               └── controller
│   │                   └── HelloController.java     # Application controller
│   └── resources
│       └── application.properties                   # Configuration file
└── test
```

## Source Code

### 1. Main Application Class
```java
package com.AL_VIS.Task1;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Task1Application {

    public static void main(String[] args) {
        SpringApplication.run(Task1Application.class, args);
    }
}
```

### 2. Application Controller
```java
package com.AL_VIS.Task1.controller;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping(value = "/")
    public String hello() {
        return "Hello Vistula, in my first Spring controller.";
    }
}
```

### 3. Configuration File
```properties
server.port=8081
spring.application.name=Task1
```

## Running the Application

1. Ensure that **JDK 17+** and **Maven** are installed.
2. Clone the project repository:
   ```bash
   git clone https://github.com/Adm0wskyyy/Spring-Zadanie1
   cd spring-zadanie1
   ```
3. Build the application using Maven:
   ```bash
   mvn clean install
   ```
4. Run the application:
   ```bash
   java -jar target/Task1-0.0.1-SNAPSHOT.jar
   ```
5. Open your browser and go to:
   ```
   http://localhost:8081/
   ```
6. You should see the message:  
   **Hello Vistula, in my first Spring controller.**

## Software Versions
- **JDK**: 17+
- **Spring Boot**: 2.7.0
- **Maven**: 3.6+

## Summary
The application successfully implements the required features, including creating a controller, changing the default port, and returning a simple response to an HTTP GET request. The project is ready for further development or integration with other systems.
