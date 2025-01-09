# Drupal 10 Project with Lando Setup

This project is a Drupal 10-based application, configured with Lando for a streamlined local development environment. Lando provides a Docker-based solution to easily run your Drupal application with minimal setup.

## Prerequisites

Before you start, ensure that you have the following tools installed:

- **[Docker](https://www.docker.com/get-started)**: Required to run the containers.
- **[Lando](https://lando.dev/)**: Simplifies the setup of local development environments.
- **[Git](https://git-scm.com/)**: Used to clone the repository and manage version control.

## Project Setup

Follow the instructions below to set up the project on your local machine.

### 1. Clone the Repository

Clone the project repository to your local machine:

```bash
git clone https://github.com/dharmendrav2/dharmendra-drupal-app.git
cd dharmendra-drupal-app
```

### 2. Start the Lando Environment

Once you're in the project directory, start the Lando environment:

```bash
lando start
```

This command will download the necessary Docker containers and set up the environment. Once the process is complete, Lando will configure the required services for your Drupal application.

### 3. Access the Drupal Site

Once Lando has finished setting up, you can access your local Drupal site at:

```bash
http://dharmendra-drupal-app.lndo.site
```

You can log in to the Drupal admin dashboard at:

```bash
http://dharmendra-drupal-app.lndo.site/user/login
```

### 4. Managing Dependencies with Composer

This project uses Composer to manage PHP dependencies. If you need to install or update dependencies, use the following command inside the Lando environment:

```bash
lando composer install
```

This will install all dependencies as defined in the `composer.json` file.

### 5. Database Setup

Lando automatically configures a database for your project. If you need to import an existing database, use the following command:

```bash
lando db-import <path_to_your_database_dump.sql>
```

### 6. Working with Lando

- To stop the Lando environment when you're done working:

  ```bash
  lando stop
  ```

- To rebuild the environment (e.g., after changing `.lando.yml` or other configuration files):

  ```bash
  lando rebuild
  ```

### 7. Available Lando Services

The following services are available in the Lando environment:

- **HTTP**: Access your Drupal site at `http://dharmendra-drupal-app.lndo.site`
- **MySQL**: Access the MySQL database using `lando mysql`
- **PHP**: Run PHP-related commands with `lando php`
- **Drush**: Run Drush commands using `lando drush`

## Customizing Your Lando Environment

You can customize the Lando environment by modifying the `.lando.yml` file. For more advanced configurations, consult the [Lando documentation](https://docs.lando.dev/).

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
