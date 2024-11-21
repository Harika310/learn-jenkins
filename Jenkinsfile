pipeline {
    agent {
        label 'agent-1'
    }
    //  Build
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is test'
            }
        }
        stage('Deploy') {
            steps {

                    sh 'echo This is deploy'
                    // error 'pipeline failed'

            }
        }
    }
// post build
    post {
        always{
            echo "This sections runs always"
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section run when pipeline failure"
        }
    }
}