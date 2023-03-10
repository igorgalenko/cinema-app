# Cinema App
The main purpose of the project is to get familiar with popular Java frameworks like Spring or Hibernate by using common OOP principles and REST api style.

The project provides an opportunity to interact with a relational database (MySQL) using a program for sending various HTTP requests (PostMan) through a web-server managed by TomCat.
Cinema App also introduces concepts such as authentication, encryption, DTO validation, transactions, relationships between entities, teaches how to solve the problems of lazy initialization and how to set access rights to certain endpoints etc.  

### Used technologies
* Maven
* Spring MVC
* Spring Security
* Spring JDBC (MySQL)
* Hibernate
* Tomcat
* N-tier architecture

### Project structure
Project structure is represented by N-tier architecture and consists of the following levels:
* controllers
* model
* service
* dao

### Model structure
![](Hibernate_Cinema_Uml.png)

### How to use
* Clone repository
* Configure [properties](src/main/resources/db.properties) of the project
* Install the MySQL database server ([instruction](https://dev.mysql.com/doc/mysql-installation-excerpt/5.7/en/)). <br>
* [Download and install](https://tomcat.apache.org/download-90.cgi) Apache Tomcat 9<br>
* [Download and install](https://www.postman.com/downloads/) PostMan for sending http request to the controllers
* Configure and start the web server
* After application is starting please login with user _admin@gmail.com_ and password _admin123_ for admin access or _user@gmail.com_ with _user123_ password for user access rights 

### HTTP requests 

| HTTP method | Endpoint   | Access level     |
|-------------|------------|------------------|
| POST        |  /register | all |
| GET         | /cinema-halls | user/admin|
| POST        | /cinema-halls | admin|
| GET         | /movies | user/admin|
| POST        | /movies | admin|
| GET         | /movie-sessions/available | user/admin|
| POST        | /movie-sessions | admin|
| PUT         | /movie-sessions/{id} | admin|
| DELETE      | /movie-sessions/{id} | admin|
| GET         | /orders | user|
| POST        | /orders/complete | user|
| PUT         | /shopping-carts/movie-sessions | user|
| GET         | /shopping-carts/by-user | user|
| GET         | /users/by-email | admin|


