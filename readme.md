# CMD VS ENTRYPOINT
## CMD Example
**To build the docker_cmd**

`docker build -t dockercmd:latest .`

**To run it**

by default it will sleep for 5 seconds

`docker run dockercmd`

Now if you want to run the sleep command for 10 seconds

`docker run dockercmd sleep 10`

So, basically it replacing the whole CMD command command of the **Dockerfile**

If you use the **CMD** command and pass command from the terminal it will fully replace the last command

## ENTRYPOINT Example

**To build the docker_cmd**

`docker build -t dockerentry:latest .`

**To run it**

by default it will sleep for 5 seconds

`docker run dockerentry`

Now if you want to run the sleep command for 10 seconds

`docker run dockerentry 10`

So, it will append the `10` to the last **CMD** and replace it

#Summary
Therefor, whatever you pass using the **ENTRYPOINT**, it appends as an extra argument command, whereas whatever command you pass for **CMD**, it replaces the whole command