1. Created github repo for project https://github.com/pankajmasaye88/Discover-Dollar-Assignment.git

2. Uploaded dockerfiles for both frontend and backend, also docker-compose file to run all three containers with port mapping.

3. Created local git on my laptop. Created dockerfiles and compose file. 
    Pushed all three files to remote github repo.

4. Added customized github actions file on Github actions.

5. Created Ubuntu vm on AWS.
    Update package list.
    Install Docker on ubunutu vm
    sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

6. Cloned github repo on ubuntu vm. Created docker images for fronted, backend and uploaded to Docker Hub.
   cd /Discover-Dollar-Assignment/backend/
    docker build . -t docker123pankaj/my-backend:latest
    docker push docker123pankaj/my-backend:latest
    (image name is dockerhub_id/image_name:tagname)

    
   cd /Discover-Dollar-Assignment/frontend/
   docker build . -t docker123pankaj/my-frontend:latest
   docker push docker123pankaj/my-frontend:latest

7. pulled mongo_db image from docker hub
   docker pull mongo:latest

8. run docker compose in detach mode to run all three containers
   docker compose up -d
   docker compose ps

9.  install nginx reverse proxy on ubuntu vm
    sudo apt install nginx -y

10. Enable port 80 inbound & outbound rules
    http port 80 tcp anywhere ipv4

11. github secrets 
   | Secret             | Value                   |
| ------------------ | ----------------------- |
| DOCKERHUB_USERNAME | Docker Hub user    |
| DOCKERHUB_TOKEN    | Docker Hub access token |
| SERVER_IP          | Cloud VM IP             |
| SERVER_USER        | ubuntu                  |
| SERVER_SSH_KEY     | VM private key     |


