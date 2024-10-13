```mermaid
erDiagram
    ADMIN {
        string ADMIN_ID
        string FIRSTNAME
        string LASTNAME
        string PHONENUMBER
        string EMAILADRESS
        string PASSWORD
        string SECURITYQUESTION
        string SECURITYANSWER
    }
    
    STUDENT {
        string STUDENT_ID
        string FIRSTNAME
        string LASTNAME
        string PHONENUMBER
        string EMAILADRESS
        string PASSWORD
        int NUMBERCOURSESREGISTERED
        bool ISFULLTIME
    }
    
    COURSE {
        string COURSE_NUMBER
        string COURSETYPE
        string COURSESECTION
        int COURSECAPACITY
        int CURRENTENROLLEMENTNUMBER
        float COURSECREDITS
        string COURSETIME
        string ONLINECOURSELINK
        string COURSEROOMNUMBER
    }
    
    REGISTERED {
        string STUDENT_ID
        string COURSE_NUMBER
    }
    
    ADMIN ||--o{ STUDENT : "manages"
    STUDENT ||--o{ REGISTERED : "registers"
    COURSE ||--o{ REGISTERED : "contains"
