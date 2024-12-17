# Zadanie1-SpringBoot

## Opis zadania
Celem zadania było stworzenie prostej aplikacji przy użyciu frameworka **Spring Boot**. Aplikacja zawiera kontroler, który obsługuje żądania HTTP GET i zwraca prostą odpowiedź. Ze względu na konflikt systemowy, port domyślny został zmieniony z `8080` na `8081`.

## Funkcjonalności aplikacji
1. **Kontroler** – obsługuje żądanie HTTP GET na głównej ścieżce (`/`) i zwraca komunikat tekstowy.
2. **Zmiana portu** – aplikacja działa na porcie `8081` zamiast domyślnego `8080`.
3. **Prosta odpowiedź** – aplikacja zwraca komunikat:
   ```
   Hello Vistula, in my first Spring controller.
   ```

## Konfiguracja portu
Port został zmieniony przez dodanie konfiguracji w pliku `application.properties`:

```properties
server.port=8081
spring.application.name=Zadanie1
```

## Struktura projektu
Poniżej przedstawiona jest struktura katalogów aplikacji:

```
src
├── main
│   ├── java
│   │   └── com
│   │       └── AL_VIS
│   │           └── Zadanie1
│   │               ├── Zadanie1Application.java     # Główna klasa aplikacji
│   │               └── controller
│   │                   └── HelloController.java     # Kontroler aplikacji
│   └── resources
│       └── application.properties                   # Plik konfiguracyjny
└── test
```

## Kod źródłowy

### 1. Główna klasa aplikacji
```java
package com.AL_VIS.Zadanie1;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Zadanie1Application {

    public static void main(String[] args) {
        SpringApplication.run(Zadanie1Application.class, args);
    }
}
```

### 2. Kontroler aplikacji
```java
package com.AL_VIS.Zadanie1.controller;

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

### 3. Plik konfiguracyjny
```properties
server.port=8081
spring.application.name=Zadanie1
```

## Uruchomienie aplikacji

1. Upewnij się, że masz zainstalowaną **JDK 17+** oraz **Maven**.
2. Sklonuj repozytorium projektu:
   ```bash
   git clone https://github.com/Adm0wskyyy/Spring-Zadanie1
   cd spring-zadanie1
   ```
3. Zbuduj aplikację za pomocą Mavena:
   ```bash
   mvn clean install
   ```
4. Uruchom aplikację:
   ```bash
   java -jar target/Zadanie1-0.0.1-SNAPSHOT.jar
   ```
5. Otwórz przeglądarkę i przejdź pod adres:
   ```
   http://localhost:8081/
   ```
6. Powinieneś zobaczyć komunikat:  
   **Hello Vistula, in my first Spring controller.**

## Wersje oprogramowania
- **JDK**: 17+
- **Spring Boot**: 2.7.0
- **Maven**: 3.6+

## Podsumowanie
Aplikacja zrealizowała założone funkcjonalności, w tym utworzenie kontrolera, zmianę domyślnego portu oraz zwrócenie prostej odpowiedzi na żądanie HTTP GET. Projekt jest gotowy do dalszego rozwijania lub integracji z innymi systemami.
# Zadanie1-SpringBoot

## Opis zadania
Celem zadania było stworzenie prostej aplikacji przy użyciu frameworka **Spring Boot**. Aplikacja zawiera kontroler, który obsługuje żądania HTTP GET i zwraca prostą odpowiedź. Ze względu na konflikt systemowy, port domyślny został zmieniony z `8080` na `8081`.

## Funkcjonalności aplikacji
1. **Kontroler** – obsługuje żądanie HTTP GET na głównej ścieżce (`/`) i zwraca komunikat tekstowy.
2. **Zmiana portu** – aplikacja działa na porcie `8081` zamiast domyślnego `8080`.
3. **Prosta odpowiedź** – aplikacja zwraca komunikat:
   ```
   Hello Vistula, in my first Spring controller.
   ```

## Konfiguracja portu
Port został zmieniony przez dodanie konfiguracji w pliku `application.properties`:

```properties
server.port=8081
spring.application.name=Zadanie1
```

## Struktura projektu
Poniżej przedstawiona jest struktura katalogów aplikacji:

```
src
├── main
│   ├── java
│   │   └── com
│   │       └── AL_VIS
│   │           └── Zadanie1
│   │               ├── Zadanie1Application.java     # Główna klasa aplikacji
│   │               └── controller
│   │                   └── HelloController.java     # Kontroler aplikacji
│   └── resources
│       └── application.properties                   # Plik konfiguracyjny
└── test
```

## Kod źródłowy

### 1. Główna klasa aplikacji
```java
package com.AL_VIS.Zadanie1;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Zadanie1Application {

    public static void main(String[] args) {
        SpringApplication.run(Zadanie1Application.class, args);
    }
}
```

### 2. Kontroler aplikacji
```java
package com.AL_VIS.Zadanie1.controller;

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

### 3. Plik konfiguracyjny
```properties
server.port=8081
spring.application.name=Zadanie1
```

## Uruchomienie aplikacji

1. Upewnij się, że masz zainstalowaną **JDK 17+** oraz **Maven**.
2. Sklonuj repozytorium projektu:
   ```bash
   git clone https://github.com/Adm0wskyyy/Spring-Zadanie1
   cd spring-zadanie1
   ```
3. Zbuduj aplikację za pomocą Mavena:
   ```bash
   mvn clean install
   ```
4. Uruchom aplikację:
   ```bash
   java -jar target/Zadanie1-0.0.1-SNAPSHOT.jar
   ```
5. Otwórz przeglądarkę i przejdź pod adres:
   ```
   http://localhost:8081/
   ```
6. Powinieneś zobaczyć komunikat:  
   **Hello Vistula, in my first Spring controller.**

## Wersje oprogramowania
- **JDK**: 17+
- **Spring Boot**: 2.7.0
- **Maven**: 3.6+

## Podsumowanie
Aplikacja zrealizowała założone funkcjonalności, w tym utworzenie kontrolera, zmianę domyślnego portu oraz zwrócenie prostej odpowiedzi na żądanie HTTP GET. Projekt jest gotowy do dalszego rozwijania lub integracji z innymi systemami.
# Zadanie1-SpringBoot

## Opis zadania
Celem zadania było stworzenie prostej aplikacji przy użyciu frameworka **Spring Boot**. Aplikacja zawiera kontroler, który obsługuje żądania HTTP GET i zwraca prostą odpowiedź. Ze względu na konflikt systemowy, port domyślny został zmieniony z `8080` na `8081`.

## Funkcjonalności aplikacji
1. **Kontroler** – obsługuje żądanie HTTP GET na głównej ścieżce (`/`) i zwraca komunikat tekstowy.
2. **Zmiana portu** – aplikacja działa na porcie `8081` zamiast domyślnego `8080`.
3. **Prosta odpowiedź** – aplikacja zwraca komunikat:
   ```
   Hello Vistula, in my first Spring controller.
   ```

## Konfiguracja portu
Port został zmieniony przez dodanie konfiguracji w pliku `application.properties`:

```properties
server.port=8081
spring.application.name=Zadanie1
```

## Struktura projektu
Poniżej przedstawiona jest struktura katalogów aplikacji:

```
src
├── main
│   ├── java
│   │   └── com
│   │       └── AL_VIS
│   │           └── Zadanie1
│   │               ├── Zadanie1Application.java     # Główna klasa aplikacji
│   │               └── controller
│   │                   └── HelloController.java     # Kontroler aplikacji
│   └── resources
│       └── application.properties                   # Plik konfiguracyjny
└── test
```

## Kod źródłowy

### 1. Główna klasa aplikacji
```java
package com.AL_VIS.Zadanie1;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Zadanie1Application {

    public static void main(String[] args) {
        SpringApplication.run(Zadanie1Application.class, args);
    }
}
```

### 2. Kontroler aplikacji
```java
package com.AL_VIS.Zadanie1.controller;

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

### 3. Plik konfiguracyjny
```properties
server.port=8081
spring.application.name=Zadanie1
```

## Uruchomienie aplikacji

1. Upewnij się, że masz zainstalowaną **JDK 17+** oraz **Maven**.
2. Sklonuj repozytorium projektu:
   ```bash
   git clone https://github.com/Adm0wskyyy/Spring-Zadanie1
   cd spring-zadanie1
   ```
3. Zbuduj aplikację za pomocą Mavena:
   ```bash
   mvn clean install
   ```
4. Uruchom aplikację:
   ```bash
   java -jar target/Zadanie1-0.0.1-SNAPSHOT.jar
   ```
5. Otwórz przeglądarkę i przejdź pod adres:
   ```
   http://localhost:8081/
   ```
6. Powinieneś zobaczyć komunikat:  
   **Hello Vistula, in my first Spring controller.**

## Wersje oprogramowania
- **JDK**: 17+
- **Spring Boot**: 2.7.0
- **Maven**: 3.6+

## Podsumowanie
Aplikacja zrealizowała założone funkcjonalności, w tym utworzenie kontrolera, zmianę domyślnego portu oraz zwrócenie prostej odpowiedzi na żądanie HTTP GET. Projekt jest gotowy do dalszego rozwijania lub integracji z innymi systemami.
