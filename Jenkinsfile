pipeline {
    agent { node { label 'agent-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo 'this is failed'
            }
        }
    }
    post { 
        always { 
            echo 'I will always run wheather the job is success or not'
        }
        success{
            echo "i will run only when job is success"
        }
        failure{
            echo "I will run only when job is failure"
        }
    }

}