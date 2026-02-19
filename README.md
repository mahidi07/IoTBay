IoTBay – IoT Devices Ordering Web Application

Project Description

IoTBay is a Java-based web application developed for managing an online IoT devices store. The system allows customers to register, browse devices, manage their profile, and view access logs. Staff users can manage device details, while administrators have full control over users and devices.

The project follows the MVC (Model-View-Controller) architectural pattern and was developed using an Agile approach with iterative releases. It is built using Java, JSP, Servlets, Maven, and MySQL.

Running the Software

Obtain the project by either cloning the repository or unzipping the folder.

Use create_database.sql to create and populate the database tables.

Use Maven to clean and compile the project:
mvn clean compile

Deploy the "target/demo" folder onto a server (e.g., Apache Tomcat).

Navigate to "target/demo/" in the browser to reach the landing page.

MySQL Setup

Download MySQL from:
MySQL :: Download MySQL Installer

Set up the MySQL server with:
Port: 3306
Password: 1111

Download the MySQL extension in VS Code (optional but recommended).

Go to the database tab.

Create a new connection using:
Port: 3306
Password: 1111

Copy everything from the create_database.sql file (in the Git repository), paste it into the SQL editor, and run the script to create the database and tables.

Login / Registration

Upon reaching the landing page, you will have two options: Login and Register.

Two types of registration are available:
2.1 You can register a customer account by filling in your details normally.
2.2 If you want to register a staff account, the staff PIN is required.
Staff PIN: 0000

To login as Admin, use the following credentials:
Email: admin@iotbay.com

Password: admin123

User Abilities

Customers:

View their profile

View the device catalog

View their access logs

Staff:

Edit device details within the catalog

Admin:

Create, update, and delete customers

Create, update, and delete staff

Create, update, and delete devices

Update account activation status

Technologies Used

Java

JSP

Servlets

Maven

MySQL

Apache Tomcat

MVC Architecture

This application was developed as part of the 41025 Introduction to Software Development course at UTS.
