# Zadanie1-SpringBoot

## Opis zadania
Celem zadania było stworzenie prostej aplikacji przy użyciu frameworka **Spring Boot**, zbudowanie pierwszego kontrolera oraz obsłużenie żądań HTTP. Dodatkowo, z powodu konfliktu systemowego, aplikacja została skonfigurowana tak, aby działała na innym porcie.

---

## **Funkcjonalności aplikacji**
1. **Kontroler** – odpowiada na żądanie HTTP GET wysyłane na główną ścieżkę (`/`).
2. **Zmieniony port** – z uwagi na konflikt systemowy domyślny port `8080` został zmieniony na **`8081`**.
3. **Prosta odpowiedź** – aplikacja zwraca komunikat:  

---

## **Konfiguracja portu**
Zmiana portu została zrealizowana poprzez dodanie odpowiedniego wpisu w pliku **`application.properties`**:
```properties

server.port=8081
spring.application.name=Zadanie1

src
│
├── main
│   ├── java
│   │   └── com.AL_VIS.Zadanie1
│   │       ├── Zadanie1Application.java  # Główna klasa aplikacji
│   │       └── controller
│   │           └── HelloController.java  # Kontroler aplikacji
│   │
│   └── resources
│       └── application.properties        # Plik konfiguracyjny
│
└── test

