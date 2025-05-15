# Train Ticket Booking System

## Overview
This is a Java-based Train Ticket Booking System that allows users to sign up, log in, view available trains, book tickets, view their bookings, and cancel tickets. The system uses JSON files for local data storage and the Jackson library for JSON parsing.

## Features
- User Sign Up and Login with password hashing
- View available trains based on source and destination
- Book train tickets
- View user booking history
- Cancel booked tickets
- JSON-based local database for users, trains, and tickets

## Technologies Used
- Java 8+
- Jackson Databind (for JSON serialization/deserialization)
- File-based JSON storage
- Maven (optional for dependency management)

## Project Structure
ticket.booking.entities // Entities like User, Train, Ticket
ticket.booking.services // Business logic for booking, user services
ticket.booking.util // Utility classes like password hashing
localDb // JSON files for storing users, trains, tickets

bash
Copy
Edit

## Setup Instructions

1. **Ensure JSON files are in place**  
   Place these files inside the `localDb` directory:  
   - `users.json`  
   - `trains.json`  
   - `tickets.json`

2. **Build and Run**  
   Compile and run the main application class or test the service classes as needed.

---

## JSON File Formats

### User (`users.json`)

```json
[
  {
    "userId": "12345",
    "name": "Amit Kumar",
    "hashedPassword": "hashed_password_here",
    "ticketsBooked": []
  }
]

Train (trains.json)
[
  {
    "trainId": "78912",
    "trainNo": "1234567",
    "seats": [[0,0,0,0,0,0],[0,0,0,0,0,0]],
    "stationTimes": {
      "Bangalore": "13:50:00",
      "Delhi": "18:00:00"
    },
    "stations": ["Bangalore", "Delhi"]
  }
]
Ticket (tickets.json)
[
  {
    "ticketId": "ABC123",
    "userId": "12345",
    "source": "Bangalore",
    "destination": "Delhi",
    "dateOfTravel": "2025-05-20T00:00:00.000+00:00",
    "train": {
      "trainId": "78912",
      "trainNo": "1234567",
      "seats": [[0,0,0,0,0,0],[0,0,0,0,0,0]],
      "stationTimes": {
        "Bangalore": "13:50:00",
        "Delhi": "18:00:00"
      },
      "stations": ["Bangalore", "Delhi"]
    }
  }
]
```
## How to Use

### Sign Up
Create a new user with a username and password.

### Login
Verify user credentials.

### Search Trains
Search available trains between two stations.

### Book Ticket
Book tickets for the selected train.

### View Bookings
List all booked tickets for a user.

### Cancel Ticket
Cancel an existing ticket.

---

## Future Enhancements

- Integrate a real database instead of JSON files.
- Add a graphical user interface or web interface.
- Implement seat selection during booking.
- Add notifications and email confirmations.

---

## Author

**Amit Kumar**  
📧 Email: [amitraj8655977@gmail.com](mailto:amitraj8655977@gmail.com)


