pipeline {
    agent { node { label 'agent-1' } }
    options {
        timeout(time: 1, unit: 'HOURS') 
    }
    environment { 
        USER = 'saikrishna'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                  ls -ltr
                  echo "hello from github push webhook event"
                  printenv
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
            steps {
                sh 'printenv'
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
