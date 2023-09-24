# GigaDB CMS

## Getting started

### Create an Environment configuration file

```
$ cp env.example.dev .env
```

### Install PHP dependencies

```
$ composer install
```

### Generate App Id and security key

```
$ docker-compose run --rm console php craft setup/app-id
$ docker-compose run --rm console php craft setup/security-key
```

### Start the service

```
$ docker-compose up -d
```

And navigate to http://localhost:8080/admin

>Note: The first time, or after the database has been destroyed, you will be redirected to http://localhost:8080/admin/install.


### Tear down the service

If you want to preserve the database:

```
$ docker-compose down
```

If you want to destroy the database:

```
$ docker-compose down --volumes
```

>Note: After destroying the database, you will need to go through the /admin/install setup again, next time you start the service
