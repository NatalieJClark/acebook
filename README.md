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

<img width="1438" alt="image" src="https://github.com/NatalieJClark/acebook/assets/107806810/cea0effb-5138-4ae1-a688-b51bd1bf42df">  


Web App Mockup:

<img width="720" alt="image" src="https://github.com/NatalieJClark/acebook/assets/107806810/c5def9bf-62a0-491b-8a03-0d4866d15d48">  


Database Schema:  

<img width="1158" alt="image" src="https://github.com/NatalieJClark/acebook/assets/107806810/bf54c31a-ac29-415c-8a24-5d9e5e19512c">


  
## Objectives
The user can:
- [x] Create an account
- [x] Log in and out
- [x] See navbar links for "Friends, "Log out" and "Acebook (newsfeed)", as well as their profile picture (which links to their profile), when they are logged in
- [x] View all users' posts
- [x] Create a post with text and/or emojis
- [x] Create a post with a picture
- [x] Like a post
- [x] Comment on a post
- [x] Send a friend request to another user
- [x] Accept friend requests from other users
- [x] See all of their friends

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
// Visit http://localhost:8080/login to log in or sign up
```
To run the tests:
```java
// Install chromedriver 
; brew install chromedriver // If you're on a Mac, Chromedriver needs to be in /usr/local/bin

// Start the server in a terminal session
; mvn spring-boot:run

// Open a new terminal session and navigate to the Acebook directory
// Run your tests in this second terminal session
; mvn test
```
