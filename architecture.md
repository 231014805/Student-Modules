```mermaid
C4Container
    title Student Module Registration System - Container Diagram

    Container(WebApp, "Web Application", "React", "User-facing interface.")
    Container(API, "API Server", "Node.js/Express", "Handles registration logic.")
    ContainerDb(Database, "Database", "MySQL", "Stores student and module data.")

    WebApp --> API
    API --> Database
