```mermaid
sequenceDiagram
    participant User
    participant App
    participant Employee

    User->>App: Open application
    App->>User: Display main interface

    User->>App: Add Employee (John Doe, 1, 50000)
    Note over User,App: Potential vulnerability: Input validation
    App->>Employee: Create Employee (John Doe, 1, 50000)
    Employee-->>App: Employee instance
    App->>App: Add Employee to list

    User->>App: Add Employee (Jane Smith, 2, 60000)
    Note over User,App: Potential vulnerability: Input validation
    App->>Employee: Create Employee (Jane Smith, 2, 60000)
    Employee-->>App: Employee instance
    App->>App: Add Employee to list

    User->>App: View Employees
    App->>App: Retrieve Employee list
    App->>User: Display Employee list
    Note over App,User: Potential vulnerability: Data exposure
