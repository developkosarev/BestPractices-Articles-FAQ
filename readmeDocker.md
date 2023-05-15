## DOCKER

##### Запуск контейнера (проверяет локальный реестр и если нет, скачивание контейнера и запуск)
> docker run hello-world
> docker run -it node

##### Просмотр всех образов (шаблоны)
> docker images | grep hello

##### Просмотр контейнеров (контейнет собирается из image)
> docker ps -a | grep node

##### Вход в контейнер и запуск команд в контейнере
> docker exec -it name-of-container_phpfpm_7 bash




## Win
https://www.pascallandau.com/blog/php-php-fpm-and-nginx-on-docker-in-windows-10/  

## Docker самый простой и понятный туториал
https://badcode.ru/docker-tutorial-dlia-novichkov-rassmatrivaiem-docker-tak-iesli-by-on-byl-ighrovoi-pristavkoi/

## Win WSL2
https://habr.com/ru/post/474346/#without-dd

## Редактор docker compose UI
https://github.com/francescou/docker-compose-ui

### DockerRailsDevelopersApplicationsEverywhere
http://onreader.mdl.ru/DockerRailsDevelopersApplicationsEverywhere/content/Ch01.html

//Запуска rails из контейнена с доступом из всей сети
rails server -b 0.0.0.0

## Docker контейнер для php
https://dev.to/martinpham/symfony-5-development-with-docker-4hj8
https://habr.com/ru/post/519500/
https://github.com/paslandau/docker-php-tutorial/tree/part_3_structuring-the-docker-setup-for-php-projects

## WSL2 Debug
https://medium.com/@tomasbruckner/intellij-xdebug-with-wsl-2-docker-4224b6efb0bb

docker pull jacobalberty/firebird:2.5-ss
docker run --name firebird_2_5-ss -d -p3050:3050 jacobalberty/firebird:2.5-ss
docker rm firebird_2_5-ss