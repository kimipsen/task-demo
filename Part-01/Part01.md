# Part 1

This exercise shows how a single task file can be accessed from multiple sub-directories and can execute commands using the current directory as working directory.
It also showcases how preconditions needs to be fullfilled before executing command.

## Try it out

Try executing the following commands (assuming you're located in the `Part-01`-directory already):

```bash
task --list-all
docker container ls

cd Compose-1
task up
docker container ls
task down

cd ..
cd Compose-2
task up
docker container ls
task down

cd ..
cd Compose-3
task up
```

## Explanation

At first we list all commands in our taskfile. This is done using `task --list-all`. It will show all commands/targets, not taking preconditions into consideration.
We then switch to the first directory, `Compose-1`. In this folder, we have a single `docker-compose.yml` along with a `.env`-file to configure a set of containers. Executing `task up` calls the command `docker compose up` in the current directory.
We show the list of containers running to show that it did in fact start up 2 containers: PostgreSQL and pgAdmin.
Executing `task down` shuts down the 2 containers, our cleanup routine.

Going into the `Compose-2`-directory, we repeat the process again, showing how we start a simple `docker-compose` containing just a single container.

Repeating the process further in the `compose-3` folder, we see that since the directory does in fact not contain a `docker-compose.yml`-file, the precondition to running `task up` fails and nothing is executed. Instead we see an error in the console.