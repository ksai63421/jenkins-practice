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
  