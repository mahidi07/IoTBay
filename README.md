# IoTBay Web Application

## Project Overview

IoTBay is a Java-based web application developed using the Model-View-Controller (MVC) architectural pattern. The system simulates an IoT device management platform where users can manage accounts and devices with strict role-based access control.

The application supports three user roles:

- Admin  
- Staff  
- Customer (User)  

Each role has clearly defined permissions to ensure proper separation of responsibilities, security, and maintainability.

This project demonstrates:
- MVC architecture implementation
- DAO pattern for database interaction
- Role-based access control
- Account activation/deactivation management
- Access log tracking (login/logout auditing)
- JUnit testing for DAO classes
- Functional testing and defect logging documentation

---

## System Architecture

The application follows the MVC pattern:

### Model Layer
- Entity classes: `User`, `Device`, `AccessLog`
- DAO classes: `UserDAO`, `DeviceDAO`, `AccessLogDAO`
- JDBC-based database communication via `DBConnector`

### View Layer
- JSP pages for UI rendering
- Role-based conditional rendering
- Form handling and user interaction

### Controller Layer
- Java Servlets for request processing
- Business logic enforcement
- Role validation and access restriction

---

## Core Features

### User Management (MVC Module)

This module allows the system administrator to manage user accounts.

Admin capabilities:
- Create users (Customer and Staff)
- View user records
- Search users by name
- Update user details
- Activate or deactivate accounts
- Delete users

Staff and Customers:
- View their own profile
- Cannot edit other users

Account activation status prevents deactivated users from logging into the system.

---

### Device Catalog Management (MVC Module)

Customer:
- View device catalog

Staff:
- Add new devices
- Edit device details
- Update stock quantities

Admin:
- Full CRUD operations on devices
- Full management access

---

### Access Log Tracking

The system automatically records:
- Login timestamp
- Logout timestamp

Users can:
- View their own access logs (read-only)

Admins may:
- View logs of other users (if permitted)

Access logs cannot be edited or deleted through the user interface.

---

## Running the Software

1. Clone the repository or download the project as a ZIP file.

2. Create the database using the provided SQL script:
   - Open `create_database.sql`
   - Execute it in MySQL

3. Compile the project using Maven:
# IoTBay Web Application

## Project Overview

IoTBay is a Java-based web application developed using the Model-View-Controller (MVC) architectural pattern. The system simulates an IoT device management platform where users can manage accounts and devices with strict role-based access control.

The application supports three user roles:

- Admin  
- Staff  
- Customer (User)  

Each role has clearly defined permissions to ensure proper separation of responsibilities, security, and maintainability.

This project demonstrates:
- MVC architecture implementation
- DAO pattern for database interaction
- Role-based access control
- Account activation/deactivation management
- Access log tracking (login/logout auditing)
- JUnit testing for DAO classes
- Functional testing and defect logging documentation

---

## System Architecture

The application follows the MVC pattern:

### Model Layer
- Entity classes: `User`, `Device`, `AccessLog`
- DAO classes: `UserDAO`, `DeviceDAO`, `AccessLogDAO`
- JDBC-based database communication via `DBConnector`

### View Layer
- JSP pages for UI rendering
- Role-based conditional rendering
- Form handling and user interaction

### Controller Layer
- Java Servlets for request processing
- Business logic enforcement
- Role validation and access restriction

---

## Core Features

### User Management (MVC Module)

This module allows the system administrator to manage user accounts.

Admin capabilities:
- Create users (Customer and Staff)
- View user records
- Search users by name
- Update user details
- Activate or deactivate accounts
- Delete users

Staff and Customers:
- View their own profile
- Cannot edit other users

Account activation status prevents deactivated users from logging into the system.

---

### Device Catalog Management (MVC Module)

Customer:
- View device catalog

Staff:
- Add new devices
- Edit device details
- Update stock quantities

Admin:
- Full CRUD operations on devices
- Full management access

---

### Access Log Tracking

The system automatically records:
- Login timestamp
- Logout timestamp

Users can:
- View their own access logs (read-only)

Admins may:
- View logs of other users (if permitted)

Access logs cannot be edited or deleted through the user interface.

---

## Running the Software

1. Clone the repository or download the project as a ZIP file.

2. Create the database using the provided SQL script:
   - Open `create_database.sql`
   - Execute it in MySQL

3. Compile the project using Maven:
# IoTBay Web Application

## Project Overview

IoTBay is a Java-based web application developed using the Model-View-Controller (MVC) architectural pattern. The system simulates an IoT device management platform where users can manage accounts and devices with strict role-based access control.

The application supports three user roles:

- Admin  
- Staff  
- Customer (User)  

Each role has clearly defined permissions to ensure proper separation of responsibilities, security, and maintainability.

This project demonstrates:
- MVC architecture implementation
- DAO pattern for database interaction
- Role-based access control
- Account activation/deactivation management
- Access log tracking (login/logout auditing)
- JUnit testing for DAO classes
- Functional testing and defect logging documentation

---

## System Architecture

The application follows the MVC pattern:

### Model Layer
- Entity classes: `User`, `Device`, `AccessLog`
- DAO classes: `UserDAO`, `DeviceDAO`, `AccessLogDAO`
- JDBC-based database communication via `DBConnector`

### View Layer
- JSP pages for UI rendering
- Role-based conditional rendering
- Form handling and user interaction

### Controller Layer
- Java Servlets for request processing
- Business logic enforcement
- Role validation and access restriction

---

## Core Features

### User Management (MVC Module)

This module allows the system administrator to manage user accounts.

Admin capabilities:
- Create users (Customer and Staff)
- View user records
- Search users by name
- Update user details
- Activate or deactivate accounts
- Delete users

Staff and Customers:
- View their own profile
- Cannot edit other users

Account activation status prevents deactivated users from logging into the system.

---

### Device Catalog Management (MVC Module)

Customer:
- View device catalog

Staff:
- Add new devices
- Edit device details
- Update stock quantities

Admin:
- Full CRUD operations on devices
- Full management access

---

### Access Log Tracking

The system automatically records:
- Login timestamp
- Logout timestamp

Users can:
- View their own access logs (read-only)

Admins may:
- View logs of other users (if permitted)

Access logs cannot be edited or deleted through the user interface.

---

## Running the Software

1. Clone the repository or download the project as a ZIP file.

2. Create the database using the provided SQL script:
   - Open `create_database.sql`
   - Execute it in MySQL

3. Compile the project using Maven:
  - mvn clean install

4. Deploy the generated `target/demo` directory to Apache Tomcat.

5. Start Tomcat.

6. Open the browser and navigate to:
   http://localhost:8080/demo/


---

## Login and Registration

Upon reaching the landing page, you may choose:

- Login
- Register

### Registration Types

Customer Registration:
- Fill in details normally.

Staff Registration:
- Requires staff PIN:
    0000

If the PIN matches, the account is created as a Staff account.
Otherwise, it defaults to a Customer account.

### Admin Login Credentials

  Email: admin@iotbay.com
  Password: admin123


---

## Role-Based Permissions

### Customer
- View profile
- View device catalog
- View access logs

### Staff
- All customer permissions
- Edit device details
- Manage stock

### Admin
- Create, update, delete users
- Activate/deactivate accounts
- Full device management
- System-level control

---

## Database Setup (MySQL)

1. Download MySQL from:
   https://dev.mysql.com/downloads/installer/

2. Install MySQL Server with:
   - Port: 3306
   - Password: 1111

3. Open MySQL Workbench or the VS Code MySQL extension.

4. Create a new connection:
   - Host: localhost
   - Port: 3306
   - Username: root
   - Password: 1111

5. Open `create_database.sql` from the repository.

6. Execute the script to create and populate all tables.

---

## Testing

### Unit Testing

JUnit test cases are provided for:
- UserDAO
- DeviceDAO

These tests validate:
- CRUD operations
- Database updates
- Search functionality
- Stock updates
- User activation updates

### Functional Testing

Manual test case documentation includes:
- Role-based validation tests
- Account activation/deactivation tests
- Device management validation
- Access log validation

### Defect Logs

The project includes structured defect documentation covering:
- Identified issues
- Root cause description
- Responsible developer
- Resolution status

---

## Security Implementation

- Prepared statements used for all SQL queries
- Role validation enforced in Servlets
- Session-based authentication
- Account status validation during login
- Read-only access to access logs
- Unauthorized access redirection

---

## Technical Stack

- Java 17+
- JSP / Servlets
- Apache Tomcat 10+
- MySQL 8+
- Maven 3.8+
- JDBC

---

## Deployment Notes

- Ensure MySQL server is running before starting Tomcat.
- Verify database credentials in `DBConnector`.
- Confirm port 3306 is available.
- Check Tomcat logs if deployment errors occur.

---

## Summary

IoTBay is a full MVC-based web application demonstrating:

- Structured backend architecture
- Role-based access control
- Secure database operations
- Account lifecycle management
- Access auditing system
- DAO pattern implementation
- Comprehensive testing practices

This project showcases complete backend web development using Java EE technologies and sound software engineering principles.


