```mermaid
C4Model
    Person(patient, "Patient")
    Person(doctor, "Doctor")
    System_Boundary(appointmentSystem, "Online Appointment System") {
        Container(webApp, "Web Application", "React", "User interface")
        Container(api, "Backend API", "Node.js", "Handles business logic")
        ContainerDb(db, "Database", "PostgreSQL", "Stores appointments and user data")
    }
    Rel(patient, webApp, "Uses")
    Rel(doctor, webApp, "Uses")
    Rel(webApp, api, "API Calls")
    Rel(api, db, "Reads/Writes")
