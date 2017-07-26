# nm-docker-symfony

## Environment

export DATABASE_HOST=mysql_server
export DATABASE_PORT=3306
export DATABASE_NAME=YOUR_DATABASE_NAME
export DATABASE_USER=YOUR_MYSQL_USER
export DATABASE_PASSWORD=YOUR_MYSQL_PASSWORD
export DATABASE_ROOT_PASSWORD=YOUR_MYSQL_ROOT_PASSWORD

## Command
`cd docker && docker-compose up -d` 
`docker exec -ti php-sf bash -c "composer create-project symfony/framework-standard-edition symfony '3.3.*'"`

parameters:
    database_host: "%env(DATABASE_HOST)%"
    database_port: "%env(DATABASE_PORT)%"
    database_name: "%env(DATABASE_NAME)%"
    database_user: "%env(DATABASE_USER)%"
    database_password: "%env(DATABASE_PASSWORD)%"
    
## Allow docker-machine IP 

in web/app_dev.php & web/config.php add 192.168.99.1 in restricted IPs list
