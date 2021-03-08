# demo_docker

## install docker-compose

dowload docker-compose
> sudo curl -L "https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

Apply executable permissions to the binary

> sudo chmod +x /usr/local/bin/docker-compose

## build a project

generate the Rails skeleton app using docker-compose run

> docker-compose run --no-deps web rails new . --force --database=postgresql

change the ownership of the new files.

> sudo chown -R $USER:$USER .

you can build again if you change dockerfile or docker-compose

> docker-compose build

boot the app with docker-compose up:

> docker-compose up

you need to create the database. In another terminal

> docker-compose run web rake db:create

## View the Rails welcome page!
![image](https://user-images.githubusercontent.com/43668977/110286920-48918980-8018-11eb-8545-8b85458b4da8.png)