## Jenkins-example


# Basic Commands

Start the Jenkins service:
    brew services start jenkins-lts

Restart the Jenkins service:
    brew services restart jenkins-lts

Stop the Jenkins service:
    brew services stop jenkins-lts

Update the Jenkins version:
    brew upgrade jenkins-lts

# Jenkins Docker Prerequisites

To use Docker in Jenkins Pipelines, you need to first install the following Docker resources
1. Docker plugin
2. Docker Pipelines

Installable from Jenkins UI 'Manage Jenkins' section

# Jenkins Docker Registry

Pull and Run local Docker Registry Container:
    docker run -d -p 5000:5000 --restart always --name registry registry:2

Tag a local Docker Image for Local Registry:
    docker tag local-image localhost:5000/gcc/sample:latest

Push Tagged Image to Local Registry:
    docker push localhost:5000/gcc/sample:latest

# Configuration examples

## Clone GitHub Repository

1. Create Freestyle Job
2. Under Source Code Management, select Git
3. Input the Github Repository URL and Credentials (no creds needed if Public)
4. Save and Build, check Console Output for logs

# Example Links

Clone Git Repo with Jenkins:
    https://narenchejara.medium.com/create-jenkin-job-and-clone-project-from-git-b513804d3089

Docker build and Push example:
    https://www.edureka.co/community/55640/jenkins-docker-docker-image-jenkins-pipeline-docker-registry

Openshift configuration example:
    https://www.openshift.com/blog/using-openshift-pipeline-plugin-external-jenkins
