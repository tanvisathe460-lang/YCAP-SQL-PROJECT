-- FOR SELF JOIN


create database ycap1;
use ycap1;

create table employees(
emp_id int primary key ,
emp_name  varchar(30),
manager_id int default 1
);

select* from employees;
insert into employees values
(1,'Suhani',null),
(2,'Runzun',1),
(3,'Ovi',1),
(4,'Samu',2);

insert into employees values
(5,'Tanvi',null),
(6,'Ayush',5),
(7,'Siddhant',5),
(8,'Swaroop',5);

select
 e.emp_name as employee,
 m.emp_name as manager
 from employees e
 left join employees m
 on e.manager_id = m.emp_id;



