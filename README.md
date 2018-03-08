# docker_service
Learning to create services using the docker-compose.yml

## Container:
- docker build -t friendlyhello .
- docker image ls
- docker run -p 4000:80 friendlyhello
- docker push username/repository:tag
- docker stack deploy -c docker-compose.yml getstartedlab
- docker service ls
- docker service ps getstartedlab_web
- docker stack rm getstartedlab

## Services:

Runing your new load-balanced app
- docker swarm init
- docker stack deploy -c docker-compose.yml getstartedlab
- docker stack rm getstartedlab
- docker leave swarm --force
- docker stack deploy
- docker swarm init --advertise-addr <myvm1 ip>

Swarm initialized: current node <node ID> is now a manager.

To add a worker to this swarm, run the following command:

  docker swarm join \
  --token <token> \
  <myvm ip>:<port>

To add a manager to this swarm, run 'docker swarm join-token manager' and follow the instructions.



## For production
* You should always set up a sepcefic version of docker on the production system
- sudo apt-get install docker-ce=<VERSION>