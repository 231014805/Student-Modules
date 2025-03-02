```mermaid
C4Component
    title Student Module Registration System - Component Diagram

    Container(WebApp, "Web Application", "React") {
        Component(Form, "Registration Form", "Allows students to register for modules.")
        Component(Selection, "Module Selection", "Lists available modules.")
        Component(Dashboard, "Dashboard", "Shows registration status.")
    }

    Container(API, "API Server", "Node.js/Express") {
        Component(Auth, "Authentication Service", "Handles user authentication.")
        Component(RegMgmt, "Registration Management", "Processes registrations.")
        Component(ModMgmt, "Module Management", "Manages module data.")
    }

    ContainerDb(Database, "Database", "MySQL") {
        Table(Students, "Students Table")
        Table(Modules, "Modules Table")
        Table(Registrations, "Registrations Table")
    }

    WebApp --> API
    API --> Database
