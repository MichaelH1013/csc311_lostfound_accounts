# Campus Lost & Found with Accounts

Name: Michael Hickey
Course: CSC 311

A Spring Boot web app where students report found items. A visitor has to register and sign in before seeing the Lost & Found page.

Built with Spring Boot, Spring Security, Thymeleaf, Spring Data JPA and an H2 database.

## How to run

You need Java 24 and Maven (IntelliJ includes Maven).

1. Open the project folder in IntelliJ and let it load the Maven project.
2. Run `LostfoundApplication`.
3. Open http://localhost:8080 in a browser.

You can also run it from a terminal in the project folder:

    mvn spring-boot:run

## How to use it

1. Opening http://localhost:8080 while signed out sends you to the sign-in page.
2. Click Register and create an account. The username needs at least 3 characters and the password at least 6.
3. Sign in with the new account.
4. Report a found item with the form, then sign out with the Sign out button.

## H2 console

Open http://localhost:8080/h2-console and use these settings:

- JDBC URL: `jdbc:h2:file:./data/lostfound-db`
- User name: `sa`
- Password: leave it empty

Then run `SELECT * FROM APP_USERS` to see the users. Passwords are stored as BCrypt hashes that start with `$2a$`.
