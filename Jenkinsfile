pipeline {
agent
    {
        node {
                label 'master'
                customWorkspace "${env.JobPath}"
              }
    }
    stages 
    {
        stage('Start') {
            steps {
                echo 'Hello'
            }
        }
        stage ('Invoke_pipelineA') {
            steps {
                build job: 'pipelineA', parameters: [
                string(name: 'param1', value: "value1")
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
