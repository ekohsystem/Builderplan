#  DevOps Project - Publishing images to Docker Hub

This is a test project to explore GitHub Action - Build & Push Action

# Goal :
Builds a Docker image and pushes it to the Cloud-hosted Docker registry (i.e. Docker Hub)

A Docker registry is a service that manages container image repositories. It allows us to do things like create repositories, push and pull images, and manage repository access. When a registry is provided via the cloud, we don't have to worry about its hosting and maintenance.

# Workflow:

![image](https://user-images.githubusercontent.com/93052750/192405807-cc8e12fc-2984-432c-87b6-df33440cbae2.png)

##### build the project

    ./gradlew build

##### build Docker image called java-app. Execute from root

    docker build -t java-app .
    
##### push image to repo 

    docker tag java-app demo-app:java-1.0
    
    
# Result:

![image](https://user-images.githubusercontent.com/93052750/192406115-c78ba691-c3fd-4718-8489-4b6526ebb58d.png)

# What can I try next?
    1) Push it to more Docker registries?
    2) How to pull image from dockerhub?
    3) Sends a Whatsapp message when code is pushed to a repository
       
![image](https://user-images.githubusercontent.com/93052750/192409264-b31200a7-958f-4c2b-916b-3a2b8b2da014.png)
       Source: https://github.com/marketplace/actions/push-notification-on-whatsapp

    
##### Credit: TechWorld with Nana and Github Marketplace

------------------------------------------------------------------------------------------------------------------------
Notes: 

Workflow Overview
* Merged code -> Test -> Build -> Deployment

How Github Actions automate these workflows? 
* When something happens IN or TO your repository (i.e. Github events), automatic Actions are exceuted in response.
* 1) Listen to EVENT
* 2) Trigger workflow

E.g. CI/CD with Github Actions
* Commit code -> Test - > Build -> Push -> Deploy
* Advantages : 
 1) Use same tool instead of 3rd party integration
 2) setup the pipeline is easy
 3) tool for developer
 4) it integrates with other technologies 
 5) Gives us the environment we specify and simply connect to target and deploy

