```mermaid
diagram C4Context
    title Student Module Registration System - Context Diagram
    
    Person(Students, "Students", "Register for modules online.")
    Person(Admin, "Administrators", "Manage module offerings and registration deadlines.")
    System(System, "Student Module Registration System", "Handles registration and module data.")

    Students --> System
    Admin --> System
