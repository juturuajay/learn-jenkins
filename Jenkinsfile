pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time:5, unit: "SECONDS")
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sleep 10
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
                //error "pipeline failure"
            }
        }
    }
    post {
        always{
            echo "this section run always"
            deleteDir()
        }
        success{
            echo "this section runs when pipeline success"
        }
        failure{
            echo "this section run when pipeline failure"
        }
    }
}