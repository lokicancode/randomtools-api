# Randomtools API

RandomTools API repo

## Useful Commands

> ### Python

1. To install dependencies from a requirements file

   `pip install -r requirements.txt`

> ### Docker

1. List docker images

   `docker image ls`

2. Remove all the images with id (bash)

   `docker rmi -f $(docker images -q)`

3. Stop all containers (bash)

   `docker stop $(docker ps -a -q)`

4. Delete all stopped containers (bash)

   `docker rm $(docker ps -a -q)`

5. Pull an image

   `docker pull ubuntu:latest`

6. Create andd run a ubuntu container with bash terminal session. also bind port 80 of the system to 80 of the container's localhost (80:80).

   `docker run --name randomtools -p 80:80 -i -t ubuntu bash`

7. Create a container and run it (two seperate commands)

   `docker create --name randomtools -p 80:80 ubuntu`

   `docker run randomtools`

8. Open new bash terminal of a running ubuntu container

   `docker exec -it randomtools bash`

9. Commit a container as image

   `docker commit --message <COMMIT_MSG> --author <AUTHOR_NAME> <CONTAINER_ID> <NEW_IMAGE_NAME>`

10. Inspect an Docker image properties

    `docker inspect <IMAGE_NAME>`

11. To see history of an image

    `docker history <IMAGE_NAME>`

12. Tag and push a image to repository.

    `docker tag local-image:tagname new-repo:tagname`

    `docker push new-repo:tagname`

    `docker tag e430914bb860 randomtools/randomtools-api:latest`

    `docker push randomtools/randomtools-api:latest`

> ### Linux bash (Ubuntu)

1. Check the shadow file if root user has hashed password

   `cat /etc/shadow | grep root`

2. Change the password of the current user

   `passwd`

3. Install a package

   `apt-get install <PACKAGE_NAME>`
