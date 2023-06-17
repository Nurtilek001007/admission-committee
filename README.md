University management system

In this project we get the reports.pdf file of accept to university.
The main method is get students of the points them take on unt.
In simple word who have more points in UNT, his are our student.

How to run the project

Integrate postgreSQL database. In application properties set your login, password and name of your database. Run and login with roles in database.


- _Packages:_
- aspect
- configuration
- controller
- dao
- entity
- exception_handling
- service
- validation


- _aspect:_
- MyLoggingAspect - aspectj method @around


- _configuration:_
- MyConfig - configuration java class
- MySecurityConfig - for auth.jdbc
- MySecurityInitializer - default class
- MyWebInitializer - default class


- _controller:_
- MvcController - for work with .jsp files
- MyController - all reports here
- MyRestController - all CRUD operations of all entity class is here


- _dao:_
- EmployeeDAO - interface of next class
- EmployeeImpl - for realizing database CRUD operations
- StudentDAO - interface of next class
- StudentDAOImp - for realizing database CRUD operations


- _entity:_
- Student - encludes next annotations: @Entity, @Table, @Column and validation annotations
- Employee - encludes next annotations: @Entity, @Table, @Column and validation annotations


- _exception_handling:_
- EmployeeGlobalExceptionHadler
- EmployeeIncorrectData
- NoSuchEmployeeException


- _service:_
- EmployeeService - interface of next class
- EmployeeServiceImpl - for extends DAO, and transaction annotation
- StudentService - interface of next class 
- StudentServiceImpl - for extends DAO, and transaction annotation


- _validation:_
- CheckEmail - interface of next class
- CheckEmailValidator - for checking email of student when input there data for report 


- _endpoints:_
- http://localhost:8080/
- http://localhost:8080/login
- http://localhost:8080/hr_info
- http://localhost:8080/manager_info
- http://localhost:8080/askDetails
- http://localhost:8080/showDetails
- http://localhost:8080/reportForEmployee
- http://localhost:8080/askDetailsStudent
- http://localhost:8080/showDetailsStudent
- http://localhost:8080/reportForStudent
- http://localhost:8080/acceptedStudents
- (get)http://localhost:8080/api/employees
- (get)http://localhost:8080/api/employees/{id}
- (post)http://localhost:8080/api/employees
- (put)http://localhost:8080/api/employees
- (delete)http://localhost:8080/api/employees/{id}
- (get)http://localhost:8080/api/students
- (get)http://localhost:8080/api/students/{id}
- (post)http://localhost:8080/api/students
- (put)http://localhost:8080/api/students
- (delete)http://localhost:8080/api/students/{id}
