pipeline {
    agent none
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            agent {
                label "slave-redhat"
            }
            when {
                branch 'dev'
            }
            steps {
                echo 'Deploying Redhat server'
            }
        }
    }
}

