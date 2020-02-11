# Docker:
	list containers `docker ps -a`
	`docker run <image>` or 
	`docker run —name <container name> <image>`
	`-a` show all
	`-q` show quite (memory location)
	`-f` filter
	`-d`runs detached in the background of 		terminal
	`-p` publish look down
	`status=` what the filter returns

	`docker image` shows all of the running 	images in the system

Publishing images to Docker `—publish`
`<hostport>:<containerExposes>`
Use the hub to find applications for different apps
	need to publish for localhost ports to 		work can run multiple instances by 			publishing on different ports

Can add a `--rm` and it will remove the container on stop


Building a custom container
`docker stop <container> `before removing it

Connecting a DB to a web app
	inspect network `docker network inspect <networkname>`
	create a docker network
		`docker network create <networkname>`
	create the container: `docker run —network <networkname> -d <containerName><imagename>`
Do this while in the root folder:
``` ### docker run --network <networkname> --name <containername> -it -p 8090:8080 -v $PWD:/root/project -w /root/project emojijournal-run sh -c .build-ubuntu/release/EmojiJournalServer
```
Explanation:
* `—name emojijournalnames` the container
* `-it … sh -c .build-ubuntu/release/EmojiJournalServercreates` an interactive terminal, and executes a shell command to run EmojiJournalServer
* `-p 8090:8080`publishes the container’s 8080 port to localhost:8090
* `-v $PWD:/root/project-mounts` the current directory in the container as/root/project—it bind your current directory to/root/project-inside the container, so changes to the host files affect the container’s files and vice versa.*Mounting Volumes*has its own section later in this tutorial.
* `-w /root/project sets` the container’s `working directory*to/root/project.-w` is short for `—workdir.`

### Docker Images Issues. 
* `docker images -a` view all images
* `docker rmi IMAGE_ID` removes an image use the IMAGE ID
* If there is an error with removing multiple children docker images use 
* `docker rmi $(docker images --filter "dangling=true” -q --no-trunc)`
` and then use `docker rmi IMAGE_ID`

# KillDocker 
Stop all containers: `docker stop (docker ps -a -q)`
Remove all containers: ``