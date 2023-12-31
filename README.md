# Team Phoenixes' Acebook Java Project

## Introduction
- I made this project with Team Phoenixes for Makers  SWE Specialism Module 2 - Engineering Project 2
- It is based on a [Makers' seed repo](https://github.com/makersacademy/acebook-java-template)
- It is a "Facebook" style site
- The application uses:
  - maven to build the project
  - thymeleaf for templating
  - flyway to manage postgres db migrations
  - selenium for feature testing
  - faker to generate fake names for testing
  - junit4 for unit testing
  - spring-security for authentication and user management
  
## Objectives
- [x] Maven:
  - [x] I can explain what pom.xml is for
  - [x] I can start the app using Maven
- [x] Thymeleaf:
  - [x] I can explain the code in `posts/index.html`
  - [x] I can plan a new template that could be used for editing a post
- [x] Flyway:
  - [x] I can explain what a migration is
  - [x] I can explain when migrations are run
  - [x] I can explain the code in the two migration files in this directory `/db/migration/`
  - [x] I can explain the naming convention for flyway migration files
- [x] Selenium:
  - [x] I can explain the code in `SignUpTest.java`
  - [x] I can write a new feature test for unsuccessful sign up
- [x] Faker:
  - [x] I can explain what Faker does
  - [x] I can explain why it's useful
- [x] JUnit4:
  - [x] I can explain the code in `PostTest.java`
  - [x] I could add more test cases to `PostTest.java`
- [x] The repository pattern:
  - [x] I can explain the repository pattern
- [x] SpringBoot:
  - [x] I can diagram how this SpringBoot application handles `GET "/posts"`
- [x] Spring Security:
  - [x] I can explain how this app is secured

## Setup
To run the app:
```java
// Clone this repository to your machine
// Open the codebase in an IDE like InteliJ or VSCode
// Create a new Postgres database called `acebook_springboot_development`
; createdb acebook_springboot_development

// Install Maven
; brew install maven

// Build the app and start the server, using the Maven command
; mvn spring-boot:run
// The database migrations will run automatically at this point
// Visit `http://localhost:8080/users/new` to sign up
```
To run the tests:
```java
// Install chromedriver
; brew install chromedriver

// Start the server in a terminal session
; mvn spring-boot:run

// Open a new terminal session and navigate to the Acebook directory
// Run your tests in this second terminal session
; mvn test
```
Common Setup Issues:
- The application is not running:  

For the feature tests to execute properly, you'll need to have the server running in one terminal session and then use a second terminal session to run the tests.

- Chromedriver is in the wrong place:  

Selenium uses Chromedriver to interact with the Chrome browser. If you're on a Mac, Chromedriver needs to be in `/usr/local/bin`. You can find out where it is like this `which chromedriver`. If it's in the wrong place, move it using `mv`.

- Chromedriver can't be opened:  

Your Mac might refuse to open Chromedriver because it's from an unidentified developer. If you see a popup at that point, dismiss it by selecting `Cancel`, then go to `System Preferences`, `Security and Privacy`, `General`. You should see a message telling you that Chromedriver was blocked and, if so, there will be an `Open Anyway` button. Click that and then re-try your tests.
