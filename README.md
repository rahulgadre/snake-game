# Running a snake-game in a Docker Container
This repository contains all the files required to a simple snake game in a docker container.

# Snake game overview
This is a snake game which can be accessed using a web browser. It's made up of a css, js, and an index.html file.

# Getting started:

# Creating folders
Before you get started with creating a container, create a master folder called snake-game or snake.
Create two folders in this master folder and name them css and js. Move the .css and .js files to their respective folders.

# Creating a source folder
Create a new folder and name it 'src' and copy the index.html and two folders into this newly created folder. 

# Creating a dockerfile

Move one directory up and download the Dockerfile at this location. At this point the master folder will have the src folder
and the dockerfile.

# Building an image

Make sure Docker service is up and running. Build an image based on the dockerfile present in the master folder.

Command: docker build -t snake-game . 
-- 
-t is used to name the image. Here the name is "snake-game".

# Starting a container

Start a container using an image that's recently created.

command: docker run -d -p 80:80 --name snake-game . 
--
. tells the command to look for the dockerfile in this location. 
port 80 has been used on the host and also on the container for the app to run. 
Change the host port to any other port as per your requirement.

# Verifying results
Once the container is up and running, open a web browser and type in either container_ip/index.html or localhost/index.html 
and check the results. Click on the start button to start the snake game.
