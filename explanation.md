Instructions
Clone this repository git clone https://github.com/Magda098/yolo
Change in to yolo directory cd yolo
Run docker compose docker-compose up
You can pass -d to the above command if you want to run in detached mode
If you need to go inside a container run the following command docker exec -it <container id> /bin/bash

Run docker ps to get the container ID
To view container logs docker logs <container id>