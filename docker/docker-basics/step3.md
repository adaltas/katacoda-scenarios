
1. Run the Alpine Linux container using `docker run alpine` 

  `alpine` is a minimal Docker image based on Alpine Linux with only 5 MB in size!

2. List running containers.

  - Why `alpine` is not on this list?

3. Run the `alpine` container using the following command: `docker run -it alpine /bin/sh`.

  - What do the `-i` and `-t` options? 
  - What does the `/bin/sh` command mean?
  - Open another terminal window and make sure the `alpine` container is currently running.

  > Tip. To terminate shell inside a container print `exit`.

4. Run a Redis container with `docker run -d redis` and execute a command inside it using `docker exec -it <CONTAINER> bash`

  - What is the difference between `docker run -it <CONTAINER> <COMMAND>` and `docker exec -it <CONTAINER> <COMMAND>`?
  - Explore the Linux filesystem inside the running containers with commands such as `pwd`, `ls`, `cd`.
  - Try to communicate with Redis: run Redis client with `redis-cli` and print `PING`. It should answer with the `PONG` message indicating that the Redis server is running.
