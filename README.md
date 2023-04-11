# Taxi service
Taxi Service is web application that performs CRUD operations with tables cars, drivers and manufacturers in database.
## Content
- [General info](#general-info)
- [Technologies](#technologies)
- [How to start the program](#how-to-start-the-program)
- [Project structure](#project-structure)

## General info
This project allows you to manage data about the cars,
their manufacturers and drivers who can drive these cars.
The project also has authentication and registration.
This project can display/add/remove cars, drivers and manufacturers,
also, you can get some driver out of the car. 

## Technologies
- Java 11
- Maven
- Servlet API
- JDBC
- JSP technology
- JSTL
- Tomcat 9.0.73
- MySQL

## How to start the program
- Install TomCat and MySQL
- Clone the project repository to your local machine
- Run the SQL script located in src/main/resources/init_db.sql to initialize the database
- Replace the values of the URL, USERNAME and PASSWORD in ConnectionUtil for your DB
- Configure TomCat for this project
- For confidence you can run in console mvn clean package

## Project structure
- Controller:
  - Car controllers:
    - AddCarController (to create new car)
    - AddDriverToCarController (to add driver to car)
    - DeleteCarController (to delete car)
    - GetAllCarsController (to display all cars)
    - GetDriversByCarController (to display drivers by car)
    - GetMyCurrentCarsController (to display cars on current account)
    - RemoveDriverFromCarController (remove some driver from some car)
  - Driver controllers:
    - AddDriverController (to create/register driver)
    - DeleteDriverController (to delete driver)
    - GetAllDriversController (to display all drivers)
  - Manufacturers controllers:
    - AddManufacturerController (to add new manufacturer)
    - DeleteManufacturerController (to delete manufacturer)
    - GetAllManufacturersController (to display all manufacturers)
  - Account controllers:
    - LoginController (to login)
    - LogoutController (to logout)
  - IndexController (main page)
- Dao:
  - CarDaoImpl (processes car model from DB)
  - DriverDaoImpl (processes driver model from DB)
  - ManufacturerDaoImpl (processes manufacturer model from DB)
- Exception:
  - AuthenticationException 
  - DataProcessingException
  - RegistrationException
- Filer:
  - AuthenticationFilter
- Model:
  - Car (car model class)
  - Driver (driver model class)
  - Manufacturer (manufacturer class)
- Service:
  - AuthenticationServiceImpl
  - CarServiceImpl
  - DriverServiceImpl
  - ManufacturerServiceImpl
  - RegistrationServiceImpl
- Util:
  - ConnectionUtil
- Resources:
  - init_db.sql (database scripts)
- Webapp:
  - jsp files
  - css files
  - web.xml (configuration files for web application)




