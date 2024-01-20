pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                  ls -ltr
                  pwd
                  echo "hello script"
                  '''
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