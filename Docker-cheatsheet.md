# Some basic docker commands:
#### (_just a beginner guide, building as I go..._)
--------------------------------------------------------------------------------

**command**|**description**|**Notes**
:----------|:----------|:----------
`docker --version`|displays currently installed version
`docker run <imagename>`| runs the file called imagename
`docker build -t hellofromdocker .`| builds a docker image as per the 'Dockerfile' specs present in the dir (as specified by the **.**)it is executed from|-t is a tag and hellofromdocker is the name of the image we built 
`docker run -p 4000:8080 hellofromdocker`|  # Run "hellofromdocker" mapping port 4000 to 8080
`docker run -d -p 4000:8080 hellofromdocker`| same as above but runs docker in detached mode and returns the user back to the terminal prompt|Also spits out long Container ID
`docker images`| list all the images present in your machine’s local Docker image registry|
`docker image rm <image id>`|Remove specified image from local machine
`CTRL+C` in your terminal to quit|quits out of currently running docker container
`docker container ls`| outputs the short form of the currently running Container ID
`docker container ls -a`| List all containers, even those not running
`docker stop ContainerID`| stops running the container
`docker container stop <containerID>`|gracefully stop the specified container
`docker container kill <containerID>`|Force shutdown of the specified container
`docker login`| login to your DockerHub online repo
`docker tag <imagename> username/repository:tag`| tags an image called imagename for username in the DockerHub and in repo specified by repository|Tag helps docker version control your images. ex: `docker tag hellofromdocker rnair07/my-first-docker-repo:v1` 
`docker push username/repository:tag`|Uploads your tagged image(see previous command) to the registry| `ex: docker push rnair07/my-first-docker-repo:v1`
`docker container rm <containerID>`| Remove specified container from the local machine 
`docker run username/repository:tag`| pulls the docker image form online registry and runs it| Now that the repo is online, you can run from the docker image from any machine by pulling from the online registry. ex : `docker run rnair07/my-first-docker-repo:v1`






# Some useful definitions:

**image**:  a lightweight, stand-alone, executable package that includes everything needed to run a piece of software

**container**: a runtime instance of an image—what the image becomes in memory when actually executed.Containers run apps natively on the host machine’s kernel.

**Dockerfile**:  portable images are defined by something called a Dockerfile. It defines what goes on in the environment inside your container.

**DockerHub**: an online place to store/retrieve docker image files (sort of like GitHub for Git). Also has a registry for all available Docker images







