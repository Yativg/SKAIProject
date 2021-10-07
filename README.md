# SKAIProject

First we will need to deploy to install Vagrant in our system:

https://www.vagrantup.com/docs/installation (depends on your OS)


Then we will need to pull the Ubuntu18.4 box with the following:
  # vagrant box add generic/ubuntu1804

replace Vagrantfile from the repo to the relevant folder.

 # vagrant up
 # vagrant ssh
 
 
 Install Docker from the following link:
 https://docs.docker.com/engine/install/ubuntu/
 
 Install docker compose from the following link:
 https://docs.docker.com/compose/install/
 
 Pull my custom Springboot image from my repo with the following command:
 docker pull yativg/spring
 
 Pull the official image of nginx:
 docker pull nginx
 
 Download the following files from my repo to any folder(they must be in the same folder):
 docker-compose.yml
 ngingx.conf
 
 cd to the folder of the files above and run the following command:

  docker-compose up --build -d

Results:
You can try if its working by curl command:

![image](https://user-images.githubusercontent.com/45316192/136418908-91c5a887-94f5-40ad-81d4-5f0a7a7e2fa9.png)

As you can see the springboot in on port 8080 , however thank to our reverse proxy only port 8181 will expose the springboot.
