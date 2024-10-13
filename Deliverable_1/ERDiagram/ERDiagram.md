```mermaid
erDiagram
    ADMIN {
        PK ADMIN_ID
         FIRSTNAME
         LASTNAME
         PHONENUMBER
         EMAILADRESS
         PASSWORD
         SECURITYQUESTION
         SECURITYANSWER
    }
    
    STUDENT {
        PK STUDENT_ID
         FIRSTNAME
         LASTNAME
         PHONENUMBER
         EMAILADRESS
         PASSWORD
         NUMBERCOURSESREGISTERED
         ISFULLTIME
    }
    
    COURSE {
        PK COURSE_NUMBER
         COURSETYPE
         COURSESECTION
         COURSECAPACITY
         CURRENTENROLLEMENTNUMBER
         COURSECREDITS
         COURSETIME
         ONLINECOURSELINK
         COURSEROOMNUMBER
    }
    
    REGISTERED {
        PK, FK1 STUDENT_ID
        PK, FK2 COURSE_NUMBER
    }
    
    ADMIN ||--o{ STUDENT : "manages"
    STUDENT ||--o{ REGISTERED : "registers"
    COURSE ||--o{ REGISTERED : "contains"
