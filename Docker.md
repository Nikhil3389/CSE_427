## Docker Command
# Game
docker pull nadav42/minesweeper
docker images
docker run -it --rm -p 5000:5000 nadav42/minesweeper
then open localhost:5000


# Ubuntu
docker pull ubuntu
docker images
docker run -it --rm -p ubuntu
docker stop <IMAGES_ID>

# MYSQL
docker pull mysql/mysql-server:5.7
docker images
docker run --name mysql1 -e MYSQL_USER=root -e MYSQL_PASSWORD=root -e MYSQL_DATABASE=homedb -p 3306:3306 -d mysql/mysql-server:5.7 
docker exec -it mysql1 mysql -uroot -p
If you did not provide a password in docker run command then system will generate a password. To change password and give some permissions:
docker logs mysql1 2>&1 | FindStr GENERATED
docker exec -it mysql1 mysql -uroot -p
