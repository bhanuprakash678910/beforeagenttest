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
                label "some-label"
            }
            when {
                branch 'dev'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}

