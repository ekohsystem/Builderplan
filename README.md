#  DevOps Project - Docker Build & Push Action

This is a test project to explore GitHub Action

##### build the project

    ./gradlew build

##### build Docker image called java-app. Execute from root

    docker build -t java-app .
    
##### push image to repo 

    docker tag java-app demo-app:java-1.0
    

![image](https://user-images.githubusercontent.com/93052750/192405807-cc8e12fc-2984-432c-87b6-df33440cbae2.png)

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

