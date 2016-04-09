# MariaDB_Docker_Replication
Files and instructions necessary to create a MariaDB replication cluster between two Docker containers.

##Instructions
Please read the instructions file in order to get this project working. It is quite lengthy, and too long to be put into this readme.

##FAQ
###1) Whenever I use a command, I receive a prompt that says TERM environment variable not set. What is this? 

I have gotten this error a few times when working with Linux. I’m not 
exactly sure what it is. Using ‘echo $TERM’ I can see it’s set to the value 
‘dumb’, even though the system just yelled at me for an unset variable. 
Use the command “export TERM=dumb” and that should solve your 
problem.  

###2) My volume mounts aren’t working. How do I troubleshoot this? 

Make sure you're using an absolute path for the file system in the Docker 
container. Also double check for spelling. If you’re using a relative path for 
your local file system, ensure you have a period (.) in front of your path. 
It’s never a bad idea to remove the old images docker­compose creates 
and create them again. Use docker-compose rm to remove stopped 
containers. 

###3) How do I stop Docker containers? 

To stop docker containers running in docker-compose, simply press 
Ctrl+C and the containers will close. To close containers you have started 
with ‘docker run’, use ‘docker stop container_name’. 
