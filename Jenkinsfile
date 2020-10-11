pipeline {
agent any

    stages 
    {
        stage('Start') {
            steps {
                echo 'Hello'
            }
        }
        stage ('Invoke_Azure-pipeline') {
            steps {
                build job: 'azure', parameters: [
                string(name: 'ARM_SUBSCRIPTION_ID', value: $params.ARM_SUBSCRIPTION_ID)
                ]
            }
        }
        stage('End') {
            steps {
                echo 'Bye'
            }
        }
    }
}
