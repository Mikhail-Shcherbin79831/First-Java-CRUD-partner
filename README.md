# First-Java-CRUD

A simple CRUD (Create, Read, Update, Delete) application written in Java, based on the
Spring guide [Creating CRUD UI with Vaadin](https://spring.io/guides/gs/crud-with-vaadin/).

## Tech stack

- Java 21
- Spring Boot 4 (Spring Data JPA)
- Vaadin 25 (web UI written in pure Java)
- H2 in-memory database

## Project structure

```
src/main/java/com/example/crudwithvaadin/
├── CrudwithvaadinApplication.java  # entry point, loads demo data on startup
├── Customer.java                   # JPA entity (id, firstName, lastName)
├── CustomerRepository.java         # Spring Data repository (database access)
├── MainView.java                   # main page: filter, grid, "New customer" button
└── CustomerEditor.java             # form to create / edit / delete a customer
doc/                                # screenshots documenting the assignment
```

## How to run

Requirements: JDK 21 or newer. Maven doesn't need to be installed; the Maven wrapper is included.

```bash
# Windows
mvnw.cmd spring-boot:run

# Linux / macOS
./mvnw spring-boot:run
```

Then open <http://localhost:8080> in a browser.

## Features

- **Create**: click *New customer*, fill in the form, click *Save*
- **Read**: all customers are listed in the grid; filter by last name with the text field
- **Update**: select a customer in the grid, change the fields, click *Save*
- **Delete**: select a customer in the grid and click *Delete*

## Documentation

Screenshots are in the [`doc`](doc/) directory.
