# Database

## Tables

### Roles Table

| Column | Data Type           | Constraints |
|--------|---------------------|-------------|
| id     | bigint              | Primary Key |
| name   | character varying(45)| Not Null    |

- The roles table is used to store information about user roles in the system.
- Each role has a unique identifier (id) and a name (name).

### Users Table

| Column   | Data Type           | Constraints |
|----------|---------------------|-------------|
| id       | bigint              | Primary Key |
| email    | character varying   | Not Null    |
| password | character varying   | Not Null    |
| name     | character varying   | Not Null    |
| surname  | character varying   | Not Null    |

- The users table holds user details, such as user ID (id), email, password, name, and surname.

### User_Roles Table

| Column  | Data Type | Constraints |
|---------|-----------|-------------|
| user_id | bigint    | Not Null    |
| role_id | bigint    | Not Null    |

- The user_roles table establishes a many-to-many relationship between users and roles.
- It contains user ID (user_id) and role ID (role_id), forming foreign key constraints to the users and roles tables.

### Stations Table

| Column | Data Type           | Constraints |
|--------|---------------------|-------------|
| id     | bigint              | Primary Key |
| name   | character varying(45)| Not Null    |
| city   | character varying(45)| Not Null    |

- The stations table represents train stations with attributes like station ID (id), name (name), and city (city).

### Trains Table

| Column              | Data Type | Constraints |
|---------------------|-----------|-------------|
| id                  | bigint    | Primary Key |
| departure_station_id| bigint    | Not Null    |
| arrival_station_id  | bigint    | Not Null    |
| duration            | interval  | Not Null    |
| seats               | integer   | Not Null    |
| train_number        | character varying | Not Null    |
| current_station_id  | bigint    | Not Null    |

- The trains table stores information about trains.
- Attributes include train ID (id), departure and arrival station IDs, duration, available seats, train number, and current station ID.

### Schedules Table

| Column          | Data Type                 | Constraints |
|-----------------|---------------------------|-------------|
| id              | bigint                    | Primary Key |
| train_id        | bigint                    | Not Null    |
| arrival_time    | timestamp without time zone| Not Null    |
| occupied_seats  | integer                   | Not Null    |
| departure_time  | timestamp without time zone| Not Null    |

- The schedules table stores information about train schedules.
- It includes details such as schedule ID (id), train ID (train_id), arrival and departure times, and the number of occupied seats.

### Tickets Table

| Column      | Data Type | Constraints |
|-------------|-----------|-------------|
| id          | bigint    | Primary Key |
| user_id     | bigint    | Not Null    |
| schedule_id | bigint    | Not Null    |
| seat_number | integer   | Not Null    |

- The tickets table contains information about tickets purchased by users.
- It includes details like ticket ID (id), user ID (user_id), associated schedule ID (schedule_id), and seat number (seat_number).