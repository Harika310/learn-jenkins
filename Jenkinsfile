pipeline {
    agent {
        label 'agent-1'
    }
    options{
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    //  Build
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                // sh sleep 10
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
            deleteDir()
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section run when pipeline failure"
        }
    }
}