# MYMZ TEAM Bus Station Database Project

## Overview
The Bus Station Database Project aims to create a comprehensive and efficient system for managing the operations of a bus station. The project will develop a database that encompasses various entities such as persons, users, drivers, tickets, buses, routes, and checkpoints. The database will facilitate ticket booking, user management, bus allocation, and route tracking functionalities.

## Team Members
- Yousef Jarbou (20200306)
- Mohammad Inshasi (20200841)
- Zaid Abdullah (20200284)
- Mohammad Kharroub (20200244)

## Description
The core entities in the database include "Person," which represents individuals associated with the bus station. A person is identified by their ID and has attributes such as name (first name and last name), birthdate, age, email, password, and mobile number. Persons can either be classified as "Users" or "Drivers," but not both simultaneously. Users have an additional attribute of an ID, while drivers have their driving license type recorded.

Tickets play a crucial role in the system and are categorized as "Economy" or "VIP." Each ticket is assigned a unique ID and features attributes such as price, status, departure time, expiry date, and activation date. Economy tickets include a discount, while VIP tickets provide meals during the journey.

Buses are represented by their ID and a corresponding number. Each bus is assigned a driver, referenced by the driver's ID, and travels through a specific route. The route entity consists of an ID, pick-up point, arrival point, and may have multiple checkpoints along the way.

By implementing the Bus Station Database Project, the bus station will benefit from streamlined ticket booking processes, efficient user management, accurate bus allocation, and effective route tracking. The database system will enhance overall operational efficiency, resulting in improved service delivery and customer satisfaction.

## Requirements (Tables)

1. **Person Table**:
   - ID (Primary Key)
   - First Name
   - Last Name
   - Birthdate
   - Age
   - Email
   - Password
   - Mobile Number

2. **User Table**:
   - ID (Foreign Key referencing Person)
   - Parent ID (Foreign Key referencing User)

3. **Driver Table**:
   - ID (Foreign Key referencing Person)
   - Driving License Type

4. **Ticket Table**:
   - ID (Primary Key)
   - Price
   - Status
   - Departure Time
   - Expiry Date
   - Activation Date
   - Type (Economy or VIP)
   - Discount (only for economy tickets)
   - Meals (only for VIP tickets)

5. **Bus Table**:
   - ID
   - Number
   - Driver ID (Foreign Key referencing Driver)
   - Route ID (Foreign Key referencing Route)

6. **Route Table**:
   - ID
   - Pick-up Point
   - Arrival Point

7. **Checkpoint Table**:
   - ID
   - Route ID (Foreign Key referencing Route)
   - Checkpoint Name

## Relationships
- User (Parent) to User (Child): Each user can have one parent and multiple children.
- User to Ticket: Each user can book one or more tickets.
- Ticket to User: Each ticket can be booked by one user.
- Ticket to Bus: Each ticket belongs to one bus.
- Bus to Ticket: Each bus can have multiple tickets.
- Driver to Bus: Each driver can drive multiple buses.
- Bus to Driver: Each bus is driven by one driver.
- Bus to Route: Each bus travels through one route.
- Route to Bus: Each route can be traveled through by multiple buses.

## Flutter Interface
The project includes a Flutter mobile application for easy access to bus station functionalities. This mobile app provides a user-friendly interface for booking tickets, managing users, allocating buses, and tracking routes.


