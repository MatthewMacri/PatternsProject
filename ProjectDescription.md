# Project Description

## 1. Basic Description

This is a ***group project for up to two students***, though it can also be completed individually. If done in a team, both members must actively contribute to the project, and the same project files must be submitted by both students. A demonstration may be required at the end of the semester.

## 2.  Learning Objectives

* Develop a software product that meets user requirements.
* Design a database for storing data.
* Build a database client in Java using Java Database Connectivity (JDBC).
* Implement CRUD operations within a Java application using JDBC
* Manage and manipulate data entered by the user, keeping track of changes.
* Create an internationalized application using I18N and L10N concepts along with relevant Java classes.
* Apply design patterns learned in class and implement an MVC architecture.
* Utilize data structures, collections, and Stream processing (with Lambda expressions).
* Collaborate through a Git repository for version control, issue tracking, and team collaboration.
* Follow a Test-Driven Development (TDD) approach.

## 3. Tools to be used

1. Any preferred IDE for development.
2. SQLite for the database.
   
## 4. Design Requirements

* A clear and well-designed GUI for input and output is essential.
* Utilize relevant class libraries.
* Implement at least two design patterns introduced in the class, such as Factory, Abstract Factory, Singleton, Bridge, Memento.
* Ensure the application follows MVC architecture.
* The application must support at least two languages (e.g., French and English), using I18N Java classes like ResourceBundle and Locale.
* Choose appropriate data structures that best fit the data model.
* At least two hierarchies of classes, each one has two layers (such as User, Teacher, Student) is required for the project. 

## 5. Steps to follow

1. Create UML diagrams (ER, class, and activity diagrams).
2. Create and populate the database.
3. Design the user interface (GUI or Console).
4. Implement the MVC architecture.
5. Develop the core classes.
6. Write test class(es) using JUnit to test the controller methods. 
8. Verify if CRUD operations implemented by the methods correctly update the database.
9. Add internationalization features using at least two Locale objects.
10. Refactor the code to incorporate design patterns.

## 6. Project Deliverables

### 6.1 Deliverable 1 - Project Description:

Submit a project idea, addressing the following points:
* Scenario: Explain the scenario under which your project will operate.
* Design Paradigm: List the functionalities you plan to demonstrate.
* Expected Output: Describe the expected results and the actions the user can perform with your application.
* Git Repository: Initialize a Maven project with valid `.gitignore`, and a `README.md` file for a project description. Create a `doc` folder which contains diagrams and the the Deliverable 1 PDF.

### 6.2 Deliverable 2 - 50% Checkpoint:

Submit the source code as a `.zip` file. The application structure must be in place, with:
* Implementation of all core classes and data structures.
* Database connectivity.
* Updated Git repository.

The Git repo must be updated too.

### 6.3 Deliverable 3 - Final Submission:

Submit the complete application, including:
* Project source code (as a `.zip` file).
* Executable JAR file that includes all necessary resources to run the project without recompilation.

The Git repo must be updated too.

### 6.4 Project Report:

Submit a project report consisting of:
* Cover page with your name, project title, and course name.
* Outline/Table of Contents.
* Project Description (same as Deliverable 1).
* Program Features and Screenshots (showing how the project meets the requirements, with output and execution examples).
* Challenges (any unimplemented features or issues faced during development).
* Learning Outcomes (what you gained from the project).

## 7. Submission Requirements

1. Deliverable 1 and the Project Report should be submitted as PDF files via the Lea system.
2.	Deliverables 2 and 3 should be uploaded to the Git repository.
3.	Deliverables 2 and 3 must also be zipped and submitted via Lea.

## 8. Grading Criteria

The following criteria will be used to evaluate the project:

The project will be evaluated based on the following:

* Functionality (accuracy of output, performance, etc.)
* Robustness (handling edge cases, exceptions, and invalid inputs)
* Adherence to project specifications
* Appropriate use of data structures and the Collections API
* Correct application of design patterns, I18N, MVC, Lambda expressions, and OOP principles (e.g., information hiding, polymorphism)
* Code documentation
* Thorough testing
* Quality of presentation and completeness of output
* Appropriate use of Git for commits and collaboration
* A recentable code testing coverage
* Git repository is appropriated used.

## 9. Example Project Ideas

Here are a few sample ideas for your final project. Feel free to be creative and add unique features to make your project more engaging.

### 9.1 Airline Reservation System

* Users can search, reserve, and book airline tickets.
* Booked tickets can be managed (e.g., changed or deleted).
* Admins handle booking requests and confirmation.
* Admins maintain passenger records and generate transaction reports.

### 9.2 Course Management System

* Administrator Module: Manages administrative functions like creating student and instructor accounts, curriculum setup, employee management, etc.
* Student Module: Students can log in to view coursework, submit assignments, and receive feedback.
* Instructor Module: Instructors can log in to check assignments, communicate with students, and provide guidance.

### 9.3 Library Management System

* Librarians can maintain book records.
* Students can search for books and reserve them.
* The system tracks borrowed, issued, and returned books.

### 9.4 Online Banking System

* Customers can view account details, such as account type, balance, loan interest rates, and transaction history.
* Customers can review credit and debit transactions, including deposit and withdrawal amounts with corresponding dates.
* Managers maintain customer records.

### 9.5 Online Medical Management System

* Patients can book appointments with doctors, receive e-prescriptions, and view medical records and lab reports.
* Doctors can offer healthcare suggestions and consult patient records.
* The system can also connect users with blood and eye donors.*

### 9.6 Online Quiz Management System

* A discussion platform with quizzes on a wide range of topics.
* Users can practice quizzes before taking the actual test.
* Admins manage grades and user accounts.

### 9.7 Food Ordering System

* Users can search for, order, and pay for food.
* Admins process orders and manage requests.
* An optional driver role (e.g., Uber Eats driver) can accept and deliver food orders.

## 10. Detailed Example: Library Management System

### 10.1 Introduction

The Limited Library Management System (LLMS) is a small-scale application where librarians can add books to the catalog, issue and return books, view the catalog, and see a list of issued books. To issue a book, the librarian verifies the studentâ€™s roll number and checks the bookâ€™s availability. After issuing, the bookâ€™s information is updated in the database. Books can be searched by title, author, or publication year.

### 10.2 Functional Requirements
The system provides different services based on the user type (Student or Librarian).

1. Librarian
    1. Add a book to the catalog
    2. Issue a book
    3. Return a book
    4. View the catalog (issued and available books)
    5. View the list of issued books and the students who borrowed them.
2. Student
    1. Search books by title
    2. Search by author.
    3. Search by publication year.
    4. View the catalogue (issued and available books)
    5. Borrow a book
    6. Return a book

### 10.3 Database Structure

You can create the following tables using SQLite or write a method in your application to create and populate the tables.

1. Books table:

    ``` sql
    | SN | Title | Author | Publisher | Quantity | Issued | AddedDate |
    ```

    * `SN`: Serial Number, TEXT, primary key.
    * `Title`: Book title (cannot be`NULL`).
    * `Author`: Authorâ€™s name (cannot be`NULL`).
    * `Publisher`: Book publisher (cannot be `NULL`).
    * `Quantity`: Number of copies available.
    * `Issued`: Number of issued copies (initially set to `0`).
    * `addedDate`: Date the book was added to the catalog.
    
2. Students table:

    ```
    | StudentId | Name | Contact |
    ```

    * `StudentId`: Student roll number, primary key.
    * `Name`: Student's name
    * `Contact`: student's contact number

3. IssuedBooks table

    ``` sql
    | id | SN | StId | StName | StudentContact | IssueDate |
    ```
    * `id`: Primary key (auto-increment).
    * `SN`: Book serial number (foreign key).
    * `StId`: Student ID (foreign key).
    * `StName`: Student's name.
    * `StudentContact`: Student's contact number.
    * `IssueDate`: Date the book was issued.

### 10.4 Implementation Details

1. Methods specifications
    1. `addBook(Book)`: Adds a new book to the catalog by creating an entry in the Books table, setting the `â€œIssuedâ€` attribute to zero, and recording the current date as the addedDate.
	2. `issueBook(b: Book, s: Student)` and `borrow(b: Book)`: These methods are responsible for issuing a book to a student. First, student details are verified. If the book is available (i.e., the `â€œIssuedâ€` value is greater than `0` in the Books table), the number of available copies (Quantity) is decreased by one, and the number of issued copies (Issued) is increased by one. A new record is then created in the IssuedBooks table. Both methods return true if the book is successfully issued.
	3. `returnBook(b: Book, s: Student)` and `return(b: Book)`: These methods handle the return of books. After verifying the studentâ€™s ID, the number of available copies is increased by one, and the number of issued copies is decreased by one. The corresponding entry in the IssuedBooks table is removed. Both methods return true if the book is successfully returned.
	4. `viewCatalog()`: Retrieves and returns a map of all books from the Books table. The mapâ€™s key is the bookâ€™s serial number (SN), and all books are sorted by `SN`.
	5. `viewIssuedBooks()`: Fetches all data from the IssuedBooks table and returns it as a sorted list by `SN`.
	6. `Search` Methods: These methods retrieve records from the Books table that meet specific search criteria, such as by title, author, or year of publication. The results are returned as a sorted list by `SN`.
