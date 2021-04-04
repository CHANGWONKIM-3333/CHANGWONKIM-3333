pipeline {
    agent any
     environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }
    stages {
        stage ('build') {
            steps {
                echo 'build'
            }
        }
        stage ('test: integration-&-quality') {
            steps {
                echo 'test: integration-&-quality'
            }
        }
        stage ('test: functional') {
            steps {
                echo 'test: functional'
            }
        }
        stage ('test: load-&-security') {
            steps {
                echo 'test: load-&-security'
            }
        }
        stage ('approval') {
            steps {
                echo 'approval'
            }
        }
        stage ('deploy:prod') {
            steps {
                echo 'deploy:prod'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
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
