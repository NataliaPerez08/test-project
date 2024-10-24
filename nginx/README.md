Create a enviroment implementing docker compose with 4 services.
    Laravel Application
    Nginx
    MySQL
    random http docker image ()

Laravel image: must implement a alpine docker image, needs to connect to mysql, the root path must retrieve some register from the database to assert database connection. This image must communicate implementing php-fpm with nginx. Optional: The start script must automatic create the migrations and seed if this is not ready and then start the fpm server

Nginx: All the request from the domain devops.test must be attended by the laravel service, except the path /thiio this must proxy to the random http docker image service.

Optional: if the request arrive with other domain this must be redirected to devops.test

Random HTTP Docker Image (Optional): This service must implement a docker compose profile with the name of your prefence. Its importante that docker compose up can start without this random http service, but when you execute docker compose --profile random up now the path /thiio must response the questions



A README file with setup instructions, including environment setup, database configuration, and how to run tests.

It is need to create an env file with thw variables:

MYSQL_ROOT_PASSWORD=passworD@123
MYSQL_DATABASE=database
MYSQL_USER=db_user
MYSQL_PASSWORD=passworD@123
