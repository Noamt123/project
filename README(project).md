[![CircleCI](https://circleci.com/gh/Noamt123/project.svg?style=svg)](https://circleci.com/gh/Noamt123/project)

# 1. Summary of project
In this project I ran an application within a docker container and kubernetes by running and creating and wirting 
 the commands that ran the apllication within a docker container and kubernetes. In addition to writing the code 
 for the Dockerfile. Furthermore I also edited the app.py code (the code the app was running on) so that it would
  output the prediction of the ai's calculations. 
  
# 2. Instructions on how to run the application within a docker container 

1. make sure you have the project envorment up in two seperate terminal windows 

2. run a shell script in terminal window1 by typing in the command: ./run_docker.sh

3. then once it says in terminal window1 that the app is running, run a shell script in terminal window2 by typing: 
./make_prediction.sh 

# 3. Instructions on how to run the application within a deployment with kubernetes

1. make sure you have the project environment up in two seperate terminal windows

2. run a shell script in terminal window1 by typing in the command: ./run_kubernetes.sh

3. wait a bit until the pod is deployed with the deployment (you can check by typing: kubectl get pods)

4. then repeat step 2

5. after it says that it was forwarded in terminal window2 run a shell script by typing in the command: ./make_prediction.sh

6. (optional) if you want to see the logs of the application when this is all done you type: kubectl get pods then 
you copy the name of the pod and type in: kubectl logs Name_Of_Pod

# 4. breif overview of files 

1. /.circleci/config.yml is where the code for making sure that this app is able to run with circleci is

2. everything in model data is used for the functionality of the ai

3. output_txt_files are where the output for running the application with in a docker container and with kubernetes are stored

4. Dockerfile is where the code for docker to make an image off of when the dokcer image is called to be built

5. Makefile is where testing software and software nessecary for the application to run is downloaded and implemented

6. README.md is instructions to set things up

7. app.py is the code for the application and is what the application run based off on

8. make_prediction.sh is the shell script where it gives the application data so that it do its calculations to do its desired job

9. requirements.txt is a list of software to be downloaded that is nessecary for the application to function

10. run_docker.sh a shell script used to build and run a docker image so the containerized app can function

11. run_kubernetes.sh a shell script used to build a docker image and run it with kubernetes so that the app can function

12. upload_docker.sh a shell script used to upload the previously created docker images to a docker repository
