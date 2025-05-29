pipeline {
    agent { label 'AGENT1' }
    environment { 
        PROJECT = 'expense'
        COMPONENT = 'backend'
    }
     options {
        //Disallow concurrent executions of the Pipeline.
        disableConcurrentBuilds()
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'SECONDS')
    }

    stages {
        stage('Build') {
            steps {
              script{
                sh """
                echo "Hello this is build"
                echo "Project: $PROJECT"
                sleep 15
                """
               }
            }
        }  
        
        stage('Test') {
            steps {
              script{
                sh """
                echo "Hello this is test"
                """
              }
            } 
        }
    

        stage('Deploy') {
            steps {
             script{
              sh """
                echo "Hello this is deploy"
                """
            }
          }
        }
    
     }
    
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'I will run when pipeline fail!'
        }
        success{
            echo 'I will run when pipeline is success!'
        }
    }
}