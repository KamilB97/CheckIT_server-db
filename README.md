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



## API

## GET Endpoints

**Returns lecturer schedule for current week. Response contains information about lectures dates, details (course name, course code, building and lecture hall informations, time of lecture star and lecture duration).**

#### `/api/lecturers/{lecturerId}/schedule`

**Returns course overall summary. Information returnet are: course id, code, number
of all lectures from particular course, list of students with numbers of participated lectures. The presence
numbers correspond to the order of lectures**

#### `/api/courses/{courseId}/summary`

**Returns all informations about lecture: lecture id, lecturer name, place, date, students
attendance list**

#### `/api/lectures/{lectureId}/details`

**Returns course overall summary. Information returnet are: course id, code, number
of all lectures from particular course, list of students with summed number of attendance**

#### `/api/courses/{courseId}/details`


**Return all courses that are lectured by the lecturer with dates of particular lectures**

#### `/api/lecturers/{lecturerId}/courses`

## POST Endpoints

**Mark student presence during lecture.**

#### `/api/lectures/presence`
Body example
#### {</br>

"lectureId": 6,</br>
"studentId": 2 </br>
}</br>


**login user to system**

#### `/login`

Body example
#### {</br>

"email": "111111@student.pwr.wroc.pl", </br>
"password": "12345678" </br>
} </br>


**Endpoint for user logout**

#### `/api/logout`

Body example
#### {</br>

"id" : "1", /br>
"logged" : "false" /br>
}</br>
