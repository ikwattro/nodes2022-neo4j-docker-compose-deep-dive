# Accessing the container

### attach a shell into the container

docker exec -it 04-accessing-container-neo4j-1 sh


### execute command in interactive mode

docker exec -it 04-accessing-container-neo4j-1 tail -f logs/debug.log


# Controlling the container

docker compose restart neo4j

* will restart without taking configuration changes
* preserve volumes ( the thin R/W layer)

docker compose up -d neo4j

* if there are configuration changes detected it will re-create the container with the new configuration but will preserve volume layers

docker compose down

* stops the container

docker compose down --volumes

* stops the container and remove volumes ( also the thin R/W layer )