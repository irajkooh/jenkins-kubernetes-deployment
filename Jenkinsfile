/*pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}*/


pipeline {
    
  environment {
    dockerimagename = "irajkoohi/react-app"
    dockerImage = ""
  }
    
  agent any
    
  stages {  
    stage('Checkout Source') {
      steps {
        git 'https://github.com/irajkooh/jenkins-kubernetes-deployment.git'   
      }
    }
  }
  /*stage('Build image') {
      steps{
        script {
          dockerImage = docker.build dockerimagename
        }
      }
    }
    stage('Pushing Image') {
      environment {
               registryCredential = 'dockerhub-credentials'
           }
      steps{
        script {
          docker.withRegistry( 'https://registry.hub.docker.com', registryCredential ) {
            dockerImage.push("latest")
          }
        }
      }
    }
    stage('Deploying React.js container to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "deployment.yaml", "service.yaml")
        }
      }
    }
  }
}*/





