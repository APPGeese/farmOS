# Getting started

Follow these instructions to set up a local farmOS development environment.

The only requirements are [Docker](https://www.docker.com) and
[Docker Compose](https://docs.docker.com/compose).

## 1. Set up Docker containers

Run the following commands to create a farmOS directory and set up Docker
containers for farmOS and PostgreSQL:

    mkdir farmOS && cd farmOS
    curl https://raw.githubusercontent.com/farmOS/farmOS/2.x/docker/docker-compose.development.yml -o docker-compose.yml
    sudo docker-compose up -d

## 2. Install farmOS

Open `http://localhost` in a browser and install farmOS with the following
database credentials:

- Database type: **PostgreSQL**
- Database name: `farm`
- Database user: `farm`
- Database password: `farm`
- Advanced options > Host: `db`

## 3. Develop

Open the `www` directory in your favorite IDE.

## Optional

### Configure private filesystem

In order to upload files, the following line must be added to
`www/web/sites/default/settings.php`:

    $settings['file_private_path'] = 'sites/default/private/files';
