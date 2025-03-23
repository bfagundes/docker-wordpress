# WordPress Docker Setup
This repository provides a Docker Compose setup to run a local WordPress environment with MySQL and phpMyAdmin support.

## Features
- WordPress running on Apache and PHP
- MariaDB as the database
- phpMyAdmin for database management
- Persistent volumes for WordPress and MySQL data
- Configuration using `.env` file

## Project Structure
```
wordpress-docker/
├── docker-compose.yml
├── .env               # Database credentials and settings
└── README.md
```

## Setup Instructions
### 1. Clone the Repository
```bash
git clone https://github.com/your-username/wordpress-docker.git
cd wordpress-docker
```

### 2. Create a `.env` File
Create a `.env` file in the project root:
```env
MYSQL_DATABASE=wordpress_db
MYSQL_USER=wp_user
MYSQL_PASSWORD=wp_pass
MYSQL_ROOT_PASSWORD=super_secure_root
```
> Update the values as needed.

### 3. Start the Services
```bash
docker compose up -d
```

### 4. Access the Services
- WordPress: [http://localhost:8000](http://localhost:8000)
- phpMyAdmin: [http://localhost:8081](http://localhost:8081)

### 5. Tear Down
To stop and remove containers, networks, and volumes:
```bash
docker compose down -v
```

## Security Tips
- Do **not** commit your `.env` file to version control.
- Add `.env` to `.gitignore`.

## Contributing
Feel free to fork and contribute! Suggestions and pull requests are welcome.

## License
This project is licensed under the MIT License.