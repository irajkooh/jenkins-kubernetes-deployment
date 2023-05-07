pipeline {   
  environment {
    dockerImageName = "irajkoohi/react-app"
    dockerImage = ""
  }
    
  agent any
    
  stages {  
      
    stage('Checkout Source') {
      steps {
        // git 'https://github.com/Bravinsimiyu/jenkins-kubernetes-deployment.git'
        //git 'https://github.com/irajkooh/jenkins-kubernetes-deployment.git'
        
        checkout scm  // if jenkins project is setup by scm (Source Control Management)
        
        /*git branch: 'my_specific_branch',
            credentialsId: 'my_cred_id',
            url: 'https://github.com/irajkooh/jenkins-kubernetes-deployment.git'  
        //sh "ls -lat"  */
      }
    }
    
    stage('Maven Install') {
    	agent {
      	docker {
        	image 'maven:3.5.0'
        }
      }
      steps {
      	sh 'mvn clean install'
      }
    }
  
    // This Jenkins Pipeline stage will use the created Dockerfile to build a Docker image named ‘irajkoohi/react-app’.
    /*stage('Build image') {
      steps {
        script {
          dockerImage = docker.build dockerImageName
        }
      }
    }*/

    /*stage('Pushing Image') {
      environment {
        registryCredential = 'dockerhub-credentials'
        }
      steps {
        script {
          docker.withRegistry( 'https://registry.hub.docker.com', registryCredential ) {
          dockerImage.push("latest")
        }
      }
    }*/  

    /*stage('Deploying React.js container to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "deployment.yaml", "service.yaml")
        }
      }
    }*/
  }  
}


// ############## pipeline test ##############
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

