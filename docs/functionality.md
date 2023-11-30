# Functionality

## For Company Clients

### Searching for a Train

- User interface that allows clients to input the departure station (Station A), destination station (Station B), and a desired time interval.
- Implement a system that queries the database to retrieve a list of available trains matching the specified criteria.
- Display relevant information such as departure and arrival times, train number.

### Ticket Purchase

- Implement a ticket purchase process that includes a seat availability check to ensure enough free seats on the selected train.
- Verify that there is no existing passenger with the same name, surname, and date of birth on the chosen train.
- Provide a time check to restrict ticket purchases within 10 minutes of the train's scheduled departure.

### User Profile and Ticket Management

- Implement a user profile feature where clients can view their purchase history and currently held tickets.
- Display details such as train information, departure and arrival times, and seat numbers for each ticket.
- Provide an option for clients to cancel a ticket if they decide not to travel, ensuring the cancellation is allowed within a reasonable timeframe before the scheduled departure.

## For Company Employees

### Adding New Stations, Trains and Schedules

- Create a dedicated interface for employees to add new stations, trains and schedules to the system.
- When adding a new train, ensure that employees input details such as the train number, departure and arrival stations.

### Viewing Registered Passengers

- Enable employees to select a specific train and view a list of all passengers who have registered for that train.
- Display relevant passenger information, such as name, surname, and seat number.

### Viewing All Stations

- Provide a comprehensive list of all stations in the system, including details such as city and station name.
- Ensure this list serves as a quick reference for employees to monitor and manage the overall station network.

### Viewing All Trains

- Provide a comprehensive list of all trains in the system, including details such as train number, route, and schedule.
- Ensure this list serves as a quick reference for employees to monitor and manage the overall train network.

### Viewing All Schedules

- Provide a comprehensive list of all schedules in the system, including details such as train and travel time.
- Ensure this list serves as a quick reference for employees to monitor and manage the overall schedules network.