pipeline {
    agent any;

    parameters {
    }

    environment {
    }

    stages {

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

         stage('Build') {
            steps {
                echo 'Building..'
            }
        }
    }


  post {
        always {
            echo 'This will always run, so send the team a notification'
            cleanWs()
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }

  }


}