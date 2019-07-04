To build the image, execute
`docker build -t movable_mysql .`

Then run the container
`docker run -d -p 3306:3306 --name movable_mysql MYSQL_ROOT_PASSWORD=supersecret movable_mysql`

Then check your credentials on the databases (enter password)
`docker exec -it movable_mysql mysql -u root -p`

On a slow server when MySQL init seems to take too long, remove the `-d` command from `docker run` and then try to run `docker exec` on separate terminal session
`docker run -p 3306:3306 --name movable_mysql MYSQL_ROOT_PASSWORD=supersecret movable_mysql`
