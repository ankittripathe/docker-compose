# docker compose
- A tool used to run multi-container applications using a single file called docker-compose.yaml.

- Instead of running many docker run commands manually, you define everything in one YAML file and start all services with:


- docker compose -f fileName.yaml up -d
where 
-d:- deteached mode
-f:- for File
fileName.yaml :- mongodb.yaml or example.yaml
up:- Create + Start all containers from the compose file


- docker compose -f fileName.yaml down
where 
down:- Stop + Remove everything created by up