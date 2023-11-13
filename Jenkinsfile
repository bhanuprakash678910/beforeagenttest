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
                label "slave1-ub"
            }
            when {
                beforeAgent true
                branch 'master'
            }
            steps {
                sh ''' echo 'Deploying'
                apt-get update && apt-get install git -y '''
            }
        }
    }
}

