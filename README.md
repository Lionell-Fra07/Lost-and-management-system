# Lost and Found Management System

A Java web application for reporting, tracking and managing lost and found items. Built as part of a Distributed Applications module (ITHJA0-44) at Eduvos.

## Features

- Report lost and found items
- View and search the list of recorded items
- Update the status of items (e.g. lost, found, claimed)
- Data stored in a MySQL database
- Web service (JAX-WS / SOAP) exposing system functionality
- File logging of system activity and errors

> Adjust this list to match exactly what your project does.

## Tech Stack

| Layer | Technology |
|-------|------------|
| Presentation | JSP |
| Controller | Java Servlets |
| Database | MySQL |
| Web service | JAX-WS (separate project, GlassFish) |
| Server | Apache Tomcat 9 |
| Logging | Java file logging |
| IDE | NetBeans (Ant web application) |

## Architecture

```
Browser (JSP) --> Servlets --> MySQL
                     |
                     +--> JAX-WS Web Service (GlassFish)
                     |
                     +--> Log file
```

## Project Structure

```
LostAndFound/          # Web application (Tomcat)
├── Web Pages/         # JSP pages
├── Source Packages/   # Servlets and Java classes
└── Libraries/         # MySQL connector etc.

LostAndFoundService/   # JAX-WS web service (GlassFish)
```

## Setup

### Prerequisites
- JDK 8 or later
- NetBeans IDE
- Apache Tomcat 9
- GlassFish server
- MySQL Server and MySQL Connector/J

### Steps
1. Clone the repository:
   ```
   git clone https://github.com/<your-username>/<repo-name>.git
   ```
2. Create the database in MySQL and run the SQL script in `/database` (add your script here).
3. Update the database URL, username and password in the connection class.
4. Open both projects in NetBeans.
5. Deploy the web service project to GlassFish and note its WSDL URL.
6. Deploy the web application to Tomcat 9 and run it.
7. Open `http://localhost:8080/LostAndFound` in your browser.

## Logging

System events and errors are written to a log file using Java's logging API. The log location is set in the logger configuration.

## What I Learned

- Building a multi-tier web app with JSP and Servlets
- Connecting Java applications to MySQL using JDBC
- Creating and consuming a SOAP web service with JAX-WS
- Deploying across Tomcat and GlassFish
- Implementing file-based logging

## Author

Lionell Franse, IT student, Eduvos (Cape Town)
