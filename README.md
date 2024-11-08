# inception-42
My inception project for 42 using Docker to make a wordpress site wiith nginx and mariadb

## How to use

1. Clone the repository

2. Rename the .env.example file to .env and fill in the values

3. create a directory called `wordpress` and `mysql` in /home/username/ and give it the right permissions

4. Modify the `docker-compose.yml` file to match the path of the wordpress and mysql directories

5. Modify the `srcs/nginx/conf/nginx.conf` file to match the server name

6. Modify the Dockerfile `srcs/nginx/Dockerfile` to match the server name

7. Run the following command to build the docker image

```bash
	make re
```