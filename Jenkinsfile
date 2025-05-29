pipeline {
    agent { label 'AGENT1' }
    environment { 
        PROJECT = 'expense'
        COMPONENT = 'backend'
    }

    stages {
        stage('Build') {
            steps {
              script{
                sh """"
                echo "Hello this is build"
                echo "Project: $PROJECT"
                """
               }
            }
        }  
        
        stage('Test') {
            steps {
              script{
                sh """"
                echo "Hello this is test"
                """
              }
            } 
        }
    

        stage('Deploy') {
            steps {
             script{
              sh """"
                echo "Hello this is deploy"
                """
            }
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