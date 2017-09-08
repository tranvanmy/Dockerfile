# Exercise 04 How To Write Docker Compose

Write a `docker-compose` file to set up a simple stack:

- A `nginx` container based on offcial `nginx` [image](https://hub.docker.com/_/nginx/)
- A `mysql` container based on offcial `mysql:5.7` [image](https://hub.docker.com/_/mysql/)
- A  `wordpress` container based on offical `wordpress:php7.0-fpm` [image](https://hub.docker.com/_/wordpress/)
- Container `mysql` is linked with `wordpress` container (by setup environment variables: `MYSQL_ROOT_PASSWORD`, `WORDPRESS_DB_PASSWORD`, `DB_HOST`, ...)
- Container `nginx` listen on port `8080` and forward request to php-fpm that runs wordpress
