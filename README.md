# Pac App
## Project integration

### Prerequisites
In order to run this project, your prerequisites are going to be the following
* Git
* Docker (Optional)
* MySQL Server
* NodeJS
* NPM (This is for Ubuntu since it doesn't include npm with nodejs)

### Instalation
This project instalation is going to be a ez peasy lemon squeazy. First, you will proceed to clone the repository using this command
```sh
$ git clone --recurse-submodules https://github.com/juan1003/pac-app.git
```
Once you have cloned the project, go to the project's directory and run the mysql container

```sh
$ cd pac-app/
$ docker compose up -d
```
**If you are not using docker (you should) then install mysql server locally and create an admin user with all privileges**

```sh
$ mysql -uroot

mysql> CREATE USER 'admin'@'localhost' IDENTIFIED WITH mysql_native_password BY 'pass1234';
mysql> GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost';
mysql> CREATE DATABASE pac_db;
```

**NOTE: The "mysql>" is just mysql shell, don't copy it when running queries on mysql shell, please**

Once you have created the user with the privileges, run this script

```sh 
$ ./launch 
```

**Make sure you have a ```.env``` file on the ```api/``` directory with the following vars, since you will need it to run the project successfully.**
```env
NODE_ENV="development"
DB_NAME="pac_db"
DB_USER="admin"
DB_PASS="pass1234"
DB_HOST="localhost"
SECRET="NoSoSecret"
```
