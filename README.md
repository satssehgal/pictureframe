# pictureframe

This is a very simple server side picture frame web application that you could use to host photos and display them on a computer, phone, or even hang a tablet on a wall and build a rotating image picture frame. 

Simply create a folder called 'img' and place the docker-compose file in the same directory. Move any image you want into the img folder and watch it come to life on all your devices. No more SD cards or external storage needed for each device. See below for the simple docker-compose file

Tested on raspberry pi zero, 3, 3B+, 4B and OSX

`
version: '3.3' 
services: 
  picframe: 
     build: ./
     image: satssehgal/pictureframe:latest 
     ports: 
      - "5000:5000" 
     volumes: 
       - ./img:/app/static/images 
     restart: always 
`
