# Docker Setup for PHP Project

This project includes Docker configuration to run multiple instances on different ports with MySQL database.

## Prerequisites

- Docker installed on your system
- Docker Compose installed on your system

## Quick Start

### Build and Run All Instances

```bash
docker-compose up -d
```

This will start:
- **MySQL Database** on port **3307** (external) / 3306 (internal)
- PHP application instance:
  - **Port 9082**: http://localhost:9082

### Run Specific Instance

To run only one instance on a specific port:

```bash
# Run MySQL and the instance on port 9082
docker-compose up -d mysql web-9082
```

## Docker Commands

### Stop All Instances
```bash
docker-compose down
```

### Stop Specific Instance
```bash
docker-compose stop web-9082
```

### View Logs
```bash
# All instances
docker-compose logs -f

# Specific instance
docker-compose logs -f web-9080

# MySQL logs
docker-compose logs -f mysql
```

### Rebuild After Changes
```bash
docker-compose up -d --build
```

### Remove All Containers and Images
```bash
docker-compose down --rmi all
```

## Database Configuration

### MySQL Connection Details

**From your host machine:**
- Host: `localhost`
- Port: `3307` (not the standard 3306 to avoid conflicts)
- Database: `phpproject`
- Username: `phpuser`
- Password: `phppassword`
- Root Password: `rootpassword`

**From PHP containers (internal network):**
- Host: `mysql`
- Port: `3306` (internal Docker network)
- Database: `phpproject`
- Username: `phpuser`
- Password: `phppassword`

### Using Database in PHP

Include the `db-config.php` file in your PHP scripts:

```php
<?php
require_once 'db-config.php';

// Use $conn for mysqli connection
$result = $conn->query("SELECT * FROM your_table");

// Or use $pdo for PDO connection (if you uncomment that section)
?>
```

The configuration automatically reads from Docker environment variables.

## Customizing Ports

To add more instances or change ports, edit `docker-compose.yml`:

1. Copy one of the service blocks (e.g., `web-9080`)
2. Rename the service (e.g., `web-9083`)
3. Change the container name
4. Update the port mapping (e.g., `"9083:80"`)

Example:
```yaml
  web-9083:
    build: .
    container_name: php-project-9083
    ports:
      - "9083:80"
    volumes:
      - .:/var/www/html
    environment:
      - APACHE_DOCUMENT_ROOT=/var/www/html
      - DB_HOST=mysql
      - DB_PORT=3306
      - DB_NAME=phpproject
      - DB_USER=phpuser
      - DB_PASSWORD=phppassword
    depends_on:
      - mysql
    restart: unless-stopped
    networks:
      - php-network
```

## Development

The application files are mounted as volumes, so changes you make locally will be reflected immediately in the running containers without needing to rebuild.

## Troubleshooting

### Port Already in Use
If you get an error about ports already being in use, either:
1. Stop the service using that port
2. Change the port in `docker-compose.yml`

### Permission Issues
If you encounter permission issues:
```bash
sudo chown -R $USER:$USER .
```

### Container Won't Start
Check logs for errors:
```bash
docker-compose logs web-9080
docker-compose logs mysql
```

### Connect to MySQL from Host
```bash
mysql -h 127.0.0.1 -P 3307 -u phpuser -p
# Password: phppassword
```

### Access MySQL Container Shell
```bash
docker exec -it php-project-mysql mysql -u root -p
# Password: rootpassword
```
