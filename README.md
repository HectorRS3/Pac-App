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
This project instalation is going to be a ride. First you will need to install PM2 node module globally if you have not yet installed it
```sh
sudo npm install -g pm2
```
then, you will proceed to clone the repository using this command
```sh
git clone --recurse-submodules https://github.com/juan1003/pac-app.git
```
Once you have cloned the project, go to the project's directory and run it
(Using Docker)
```sh
cd pac-app/
./everything
```
(Not using Docker)
```sh
cd pac-app/
./everything-no-docker
```
**Make sure you have a ```.env``` file on the ```api/``` directory, since you will need it to run the project successfully.**
