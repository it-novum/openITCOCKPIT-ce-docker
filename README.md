# openITCOCKPIT-CE-docker

This repository contains the necessary files to run openITCOCKPIT Community Edition as a container.

It requires Docker Compose or a compatible alternative.

Please see the official documentation for more information: https://docs.openitcockpit.io/en/installation/docker

## Prerequisites
Before running openITCOCKPIT Community Edition with Docker, make sure you have the following prerequisites installed on your system:
- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started
To get started with openITCOCKPIT Community Edition using Docker, follow these steps:

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/it-novum/openITCOCKPIT-ce-docker.git
   ```

2. Navigate to the cloned repository:
   ```bash
   cd openITCOCKPIT-ce-docker
   ```

3. Run the Docker Compose command to start openITCOCKPIT:
   ```bash
   docker compose up -d
   ```

4. Wait for the containers to start and initialize the application.

5. Once the containers are up and running, you can access openITCOCKPIT Community Edition by opening a web browser and entering the following URL:
   ```
   https://localhost
   ```

6. Follow the on-screen instructions to complete the initial setup of openITCOCKPIT.

## Configuration
The configuration for openITCOCKPIT Community Edition can be modified by editing the `compose.yml` file in the repository. You can adjust settings such as database credentials, ports, and volumes according to your requirements.

Most settings can be adjusted through environment variables. Please see the file `openitcockpit.env`, which contains all available environment variables with default values.

By default, openITCOCKPIT Community Edition will expose these ports:

 - 80 (HTTP)
 - 443 (HTTPS)

The default credentials are:

- E-Mail `user@example.org`
- Password: `asdf12`

You can change the default credentials **before the first start of the docker container** through the file `openitcockpit.env`:
```sh
OITC_ADMIN_EMAIL=user@example.org
OITC_ADMIN_PASSWORD=asdf12
OITC_ADMIN_FIRSTNAME=John
OITC_ADMIN_LASTNAME=Doe
```

**If you have not changed the default credentials, you can still change the password or [create a new user](https://docs.openitcockpit.io/en/configuration/usermanagement/) afterwords.**

## Updating openITCOCKPIT
To update openITCOCKPIT Community Edition to the latest version, follow these steps:

1. Pull the latest changes from the repository:
   ```bash
   git pull origin main
   ```

2. Stop and remove the running containers:
   ```bash
   docker compose down
   ```

3. Run the Docker Compose command again to start the updated version:
   ```bash
   docker compose up --pull always -d
   ```

## Troubleshooting
If you encounter any issues or have questions regarding openITCOCKPIT Community Edition with Docker, please refer to the [official documentation](https://docs.openitcockpit.io/en/installation/docker).

## Contributing
Contributions are welcome! If you find any bugs or have suggestions for improvements, please open an issue or submit a pull request in this repository.

Bugs or issues related to openITCOCKPIT itself should be created in the corresponding repository: https://github.com/it-novum/openITCOCKPIT

## License
This project is licensed under the [MIT License](LICENSE).

## Support
For any further assistance or support, please reach out to the [openITCOCKPIT Community](https://openitcockpit.io/community/).
