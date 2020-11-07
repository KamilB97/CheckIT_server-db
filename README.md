# Description
CheckIT is software for attendance check during lectures and was created to meet needs of one of studies subjects. This part contains server application with database. The whole project was consisted of server application, browser application, database and ultimately mobile app that use NFC to check attendance. 
Server application is addapted to work with MySQL database. For test purposes application can use inner H2 database. 

## Stack
* Spring boot
* Hibernate
* MySQL
* JWT

## Technical information
* Application is compatible with Java 1.8
* Application works at localhost port 8090
* Current application.properties file is setup to work with inner H2 database. To switch into MySQL uncomment MySQL configurations in application.properties file and comment lines that regards to H2 database.
* Application automatically creates database schema if this do not exist.
* Script containing database inserts (data.sql) is located at src/main/resurces location.

## How to run server application from .jar file
In the directory where "checkIT-server.jar" file is located:

### `java -jar checkIT-server.jar`

