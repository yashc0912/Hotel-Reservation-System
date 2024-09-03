# Hotel Reservation System

## Overview

The **Hotel Reservation System** is a Java-based console application designed to manage hotel reservations efficiently. This project demonstrates the integration of core Java concepts with database management using JDBC (Java Database Connectivity). The system provides a simple yet effective interface for users to perform various reservation-related operations, including booking rooms, viewing and updating reservations, and retrieving specific reservation details. It is an excellent example of how Java can be used to develop a real-world application with database interaction.

## Features

- **Reserve a Room**: Users can reserve a room by providing the guest's name, room number, and contact details. The reservation is then stored in the MySQL database.
  
- **View Reservations**: This feature allows users to view all current reservations stored in the database. The reservations are displayed in a neatly formatted table, including details like reservation ID, guest name, room number, contact number, and the reservation date.

- **Retrieve Room Number**: Users can fetch the room number for a specific reservation by providing the reservation ID and guest name. This feature is useful for quickly locating room information without having to manually search through all reservations.

- **Update Reservation**: Users can update existing reservations by providing a new guest name, room number, or contact number. This feature ensures that reservation details can be modified as needed.

- **Delete Reservation**: Allows users to delete a reservation from the system. This is particularly useful for managing cancellations or erroneous entries.

- **Error Handling**: The system includes error handling for common issues such as invalid input, missing reservations, and database connectivity problems, ensuring a smooth user experience.

## Technologies Used

- **Java**: The core programming language used to build the application. Key concepts such as exception handling, loops, and conditional statements are employed.
  
- **JDBC (Java Database Connectivity)**: Used for connecting and interacting with the MySQL database. JDBC allows the application to execute SQL queries, retrieve results, and update the database in real-time.

- **MySQL**: The relational database management system used to store reservation data. The database schema includes tables for reservations with fields such as reservation ID, guest name, room number, contact number, and reservation date.

- **SQL**: Structured Query Language is used for creating, reading, updating, and deleting (CRUD) operations in the database.

## Installation

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- MySQL Server
- JDBC Driver for MySQL
- An Integrated Development Environment (IDE) like IntelliJ IDEA, Eclipse, or NetBeans

### Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/hotel-reservation-system.git
   cd hotel-reservation-system
   ```

2. **Set Up MySQL Database**:
   - Create a new MySQL database named `hotel_db`.
   - Create a table named `reservations` with the following schema:
     ```sql
     CREATE TABLE reservations (
         reservation_id INT AUTO_INCREMENT PRIMARY KEY,
         guest_name VARCHAR(255) NOT NULL,
         room_number INT NOT NULL,
         contact_number VARCHAR(20) NOT NULL,
         reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```
   - Insert some initial data if needed.

3. **Update Database Configuration**:
   - Open the `HotelReservationSystem.java` file.
   - Update the `url`, `username`, and `password` fields with your MySQL connection details.
   ```java
   private static final String url = "jdbc:mysql://localhost:3306/hotel_db";
   private static final String username = "your_mysql_username";
   private static final String password = "your_mysql_password";
   ```

4. **Compile and Run**:
   - Compile the Java file using your IDE or command line.
   - Run the `HotelReservationSystem` class.

## Usage

- Upon running the application, you will be presented with a menu to choose different operations.
- Select an option by entering the corresponding number.
- Follow the prompts to input data or view results.

### Example Usage

1. **Reserve a Room**:
   - Select option `1`.
   - Enter the guest name, room number, and contact number.
   - The system will confirm if the reservation was successful.

2. **View Reservations**:
   - Select option `2`.
   - The system will display all current reservations in a table format.

3. **Retrieve Room Number**:
   - Select option `3`.
   - Enter the reservation ID and guest name.
   - The system will display the corresponding room number.

4. **Update Reservation**:
   - Select option `4`.
   - Enter the reservation ID and new details to update an existing reservation.

5. **Delete Reservation**:
   - Select option `5`.
   - Enter the reservation ID to delete the reservation.

6. **Exit the System**:
   - Select option `0` to exit the application.

## Conclusion

The Hotel Reservation System is a comprehensive project that showcases the use of Java for developing a functional and interactive application. It effectively demonstrates the application of JDBC for database operations, making it a valuable learning resource for anyone interested in Java development and database integration.
