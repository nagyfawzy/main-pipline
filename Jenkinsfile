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
                string(name: 'ARM_SUBSCRIPTION_ID', value: "6405e052-5a9e-4ef1-b6fa-91088a6ba1d6")
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
