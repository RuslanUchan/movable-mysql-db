To build the image, execute
`docker build -t movable_mysql .`

Then run
`docker run -d -p 3306:3306 --name movable_mysql \
-e MYSQL_ROOT_PASSWORD=supersecret movable_mysql`
