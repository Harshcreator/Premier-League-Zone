# PremierZone

PremierZone is a Spring Boot application designed for a Premier League fantasy website. It provides RESTful APIs to manage player statistics and details.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database Configuration](#database-configuration)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/Harshcreator/Premier-League-Zone.git
    cd premier-zone
    ```

2. Build the project using Maven:
    ```sh
    ./mvnw clean install
    ```

3. Run the application:
    ```sh
    ./mvnw spring-boot:run
    ```

## Usage

Once the application is running, you can access the API at [http://localhost:8080/api/v1/player].

## API Endpoints

### Get All Players
- **URL:** `/api/v1/player`
- **Method:** `GET`
- **Description:** Retrieves a list of all players.
- **Response:**
    ```json
    [
        {
            "name": "Player Name",
            "nation": "Nation",
            "pos": "Position",
            "age": 25,
            "mp": 10,
            "starts": 8,
            "min": 720.0,
            "gls": 5.0,
            "ast": 3.0,
            "pk": 1.0,
            "crdy": 2.0,
            "crdr": 0.0,
            "xg": 4.5,
            "xag": 2.5,
            "team": "Team Name"
        }
    ]
    ```

### Get Players by Team
- **URL:** `/api/v1/player?team={teamName}`
- **Method:** `GET`
- **Description:** Retrieves a list of players from a specific team.
- **Response:** Same as above.

### Add a Player
- **URL:** `/api/v1/player`
- **Method:** `POST`
- **Description:** Adds a new player.
- **Request Body:**
    ```json
    {
        "name": "Player Name",
        "nation": "Nation",
        "pos": "Position",
        "age": 25,
        "mp": 10,
        "starts": 8,
        "min": 720.0,
        "gls": 5.0,
        "ast": 3.0,
        "pk": 1.0,
        "crdy": 2.0,
        "crdr": 0.0,
        "xg": 4.5,
        "xag": 2.5,
        "team": "Team Name"
    }
    ```

### Update a Player
- **URL:** `/api/v1/player`
- **Method:** `PUT`
- **Description:** Updates an existing player.
- **Request Body:** Same as above.

### Delete a Player
- **URL:** `/api/v1/player/{playerName}`
- **Method:** `DELETE`
- **Description:** Deletes a player by name.

## Database Configuration

The application uses PostgreSQL as the database. Configure the database connection in [application.properties](http://_vscodecontentref_/1):

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/prem_stat
spring.datasource.username=your-username
spring.datasource.password=your-password
spring.jpa.hibernate.ddl-auto=none
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request.

## License

Distributed under the MIT License. See `LICENSE` for more information.
```
