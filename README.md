# hands-on-sql-task-1-joins
practicing joins in sql

CREATE DATABASE RAOS_ACADEMY1;
use RAOS_ACADEMY;
show databases;

create table student_details(
serial_number INT,
student_name VARCHAR(100)
 );
 SHOW TABLES;
 describe student_details;
 insert into student_details (serial_number ,student_name )
 values(1,"prashanth");
 insert into student_details (serial_number ,student_name )
 values(2,"hema");
 insert into student_details (serial_number ,student_name )
 values(3,"rakesh");
select *from student_details;
 
 create table teacher_details(
serial_number_assigned INT,
teacher_name VARCHAR(100)
 );
 insert into teacher_details (serial_number_assigned ,teacher_name )
 values(1,"subbarao");
 insert into teacher_details (serial_number_assigned ,teacher_name )
 values(2,"venkatrao");
 insert into teacher_details (serial_number_assigned ,teacher_name )
 values(3,"ramarao");
 insert into teacher_details (serial_number_assigned ,teacher_name )
 values(10,"mallikarao");
select *from teacher_details ;
-- join 
-- inner join
SELECT serial_number_assigned,serial_number
FROM teacher_details 
INNER JOIN student_details
ON teacher_details .serial_number_assigned = student_details.serial_number;
-- leftjoin
SELECT serial_number_assigned,serial_number
FROM teacher_details 
left JOIN student_details
ON teacher_details .serial_number_assigned = student_details.serial_number;
-- right join
SELECT serial_number_assigned,serial_number
FROM teacher_details 
right JOIN student_details
ON teacher_details .serial_number_assigned = student_details.serial_number;
 
