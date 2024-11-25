A Docker Compose configuration that sets up MariaDB, PostgreSQL, MongoDB, and multiple web-based database management tools (Adminer for SQL databases and Mongo Express for MongoDB).



I've created a Docker Compose configuration that sets up a complete database development environment. Here's what's included and how to use it:

1. **Databases**:
   - MariaDB (port 3306)
   - PostgreSQL (port 5432)
   - MongoDB (port 27017)

2. **Management Interfaces**:
   - Adminer (port 8080) - for MariaDB and PostgreSQL
   - Mongo Express (port 8081) - for MongoDB

3. **Key Features**:
   - Persistent data storage using named volumes
   - Secure network isolation using a custom bridge network
   - Environment variables for easy configuration
   - Automatic container restart policy
   - Basic authentication for added security

To use this configuration:

1. Save the content to a file named `docker-compose.yml`
2. Run the following command in the same directory:
```bash
docker compose up -d
```

Access the management interfaces:
- Adminer: http://localhost:8080
  - System: Choose MariaDB/PostgreSQL
  - Server: Use service name (mariadb/postgres)
  - Username: user
  - Password: password

- Mongo Express: http://localhost:8081
  - Username: admin
  - Password: pass

Default credentials:
- MariaDB:
  - User: user
  - Password: password
  - Root Password: rootpassword

- PostgreSQL:
  - User: user
  - Password: password

- MongoDB:
  - Root Username: root
  - Root Password: rootpassword

To stop the services:
```bash
docker compose down
```

To stop and remove all data:
```bash
docker compose down -v
```

Would you like me to make any adjustments to the configuration or explain any part in more detail?