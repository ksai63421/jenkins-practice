pipeline {
    agent { node { label 'agent-1' } }
     options {
        timeout(time: 1, unit: 'HOURS') 
    }
    environment { 
        USER = 'SAIKRISHNA'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                ls -ltr
                pwd
                echo "Hello frrom github push webhook evnt"
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
            }
        }
    }
     post { 
        always { 
            echo 'I will always run whether job is success or not'
        }
        success{
            echo'I will only when job is success'
        }
        failure{
            echo'I will run when job is failure'
        }
    }
}
  