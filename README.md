# Introduction
This is a sample that shows how to use nginx and another api server in a docker compose setup.

# Setup
1. Make sure you have docker installed on the target machine.
2. Clone this repository.
3. Make sure `docker-compose` command is available and added to the path.
4. Add the following host file entry in `/etc/hosts`
```
127.0.0.1 tos.demo
```

# Instructions for running it on local machine.
At the folder where this repository is cloned, 
```
docker-compose  up -d --build
```
The nginx server is live at port `8080`. 
You can open this link once everything is done [http://tos.demo:8080](http://tos.demo:8080).

# Clean up 
At the root of this repository
```
docker-compose down
```
# Instruction to run it remotely.
Change the `server_name` in [nginx.conf](./nginx/nginx.conf) file to domain where you expect the application to be hosted at.
