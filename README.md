# Task1-SpringBoot

## Task Description
The goal of this task was to create a simple application using the **Spring Boot** framework. The application includes a controller that handles HTTP GET requests and returns a simple response. Due to a system conflict, the default port has been changed from `8080` to `8081`.

## Application Features
1. **Controller** – handles HTTP GET requests on the root path (`/`) and an additional `/greeting` path.
2. **Port Configuration** – the application runs on port `8081` instead of the default `8080`.
3. **Dynamic Response** – the application returns messages:
   - At root (`/`):
     ```
     Hello Vistula, in my first Spring controller.
     ```
   - At `/greeting` with an optional `name` parameter:
     ```
     Hello, {name}!
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
│       ├── static
│       │   └── images
│       │       └── port_1.jpg                       # Static image resource
│       └── templates
│           └── greeting.html                        # Thymeleaf template
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

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@Controller
public class HelloController {

    @GetMapping(value = "/")
    public String hello() {
        return "Hello Vistula, in my first Spring controller.";
    }

    @GetMapping("/greeting")
    public String greeting(@RequestParam(name = "name", required = false, defaultValue = "World") String name, Model model) {
        model.addAttribute("name", name);
        return "greeting";
    }
}
```

### 3. Thymeleaf Template (`greeting.html`)
```html
<!DOCTYPE HTML>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <title>Greeting Page</title>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
</head>
<body>
    <h1 th:text="'Hello, ' + ${name} + '!'">Hello!</h1>
    
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas vestibulum dignissim malesuada.
    </p>

    <img th:src="@{/images/port_1.jpg}" alt="Port" width="600" height="600"/>
</body>
</html>
```

### 4. Configuration File
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
   - Root path: `http://localhost:8081/`
   - Greeting path: `http://localhost:8081/greeting?name=YourName`

6. You should see:
   - Root: **Hello Vistula, in my first Spring controller.**
   - Greeting: **Hello, YourName!**

## Software Versions
- **JDK**: 17+
- **Spring Boot**: 2.7.0
- **Maven**: 3.6+

## Summary
The application successfully implements additional features, including a controller with dynamic responses using Thymeleaf templates and a static image resource. The project is ready for further development or integration with other systems.
