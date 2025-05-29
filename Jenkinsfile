pipeline {
    agent { label 'AGENT1' }

    stages {
        stage('Build') {
            steps {
                echo 'Hello this is build'
            }
        }  
        stage('Test') {
            steps {
                echo 'Hello this is test'
            }
        }
    

        stage('Deploy') {
            steps {
                echo 'Hello this is deploy'
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