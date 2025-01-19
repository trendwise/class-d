```mermaid
classDiagram
    class App {
        -List~Employee~ employees
        +App()
        +void addEmployee(Employee employee)
        +List~Employee~ getEmployees()
        +static void main(String[] args)
    }

    class Employee {
        -String name
        -int id
        -double salary
        +Employee(String name, int id, double salary)
        +String getName()
        +void setName(String name)
        +int getId()
        +void setId(int id)
        +double getSalary()
        +void setSalary(double salary)
        +String toString()
    }

    App --> Employee
