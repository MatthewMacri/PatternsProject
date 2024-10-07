```mermaid
flowchart TD
A["Student Accesses Registration System"] --> B["Register for Courses"]
A --> C["View Course Schedule"]
A --> D["Drop Courses"]
B --> E["Check Course Availability"]
E --> F["Course Available?"]
F -- Yes --> G["Register Student for Course"]
F -- No --> H["Display Error: Course Full"]
G --> I["Confirm Registration"]
D --> J["Confirm Course Drop"]

subgraph Admin Actions Part 1
    K["Admin Accesses System"] --> L["Add/Update/Remove Courses"]
end

subgraph Admin Actions Part 2
    L --> M["Manage Student Enrollments"]
    M --> N["Generate Reports"]
end