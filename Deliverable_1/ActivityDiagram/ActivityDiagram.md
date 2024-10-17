```mermaid
flowchart TD
%% Login decision
A["Student, Teacher, or Admin Login"] --> |Student| B["Student Accesses Registration System"]
A --> |Teacher| Q["Teacher Accesses System"]
A --> |Admin| K["Admin Accesses System"]

%% Student actions
B --> C["Register for Courses"]
B --> D["View Course Schedule"]
B --> E["Drop Courses"]
C --> F["Check Course Availability"]
F --> G["Course Available?"]
G -- Yes --> H["Register Student for Course"]
G -- No --> I["Display Error: Course Full"]
H --> J["Confirm Registration"]
E --> L["Confirm Course Drop"]

%% Teacher actions
Q --> R["View Course Details"]
R --> S["View Student List"]
R --> T["View Class Schedule"]

%% Admin actions
K --> M["Create/Remove Admins or Students"]
K --> N["Add/Update/Remove Courses"]
K --> O["Manage Student Enrollments"]
N --> P["Generate Schedule"]
