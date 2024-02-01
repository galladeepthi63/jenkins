pipeline {
    agent {
        node {
            label 'AGENT-1'
            
        }
    }
    environment { 
        GREETING = 'Hello Jenkins'
    }
    options {
        timeout(time: 1, unit: 'HOURS') 
        disableConcurrentBuilds()
    }

    stages {
        stage('Build') {
            steps {
                //
                echo "Building..."
            }
        }
        stage('Test') {
            steps {
                //
                echo "Testing..."
            }
        }
        stage('Deploy') {
            steps {
                //
                sh """
                    echo "$GREETING"
                """
            }
        }
    }
    // post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'This run when pipeline failed ,get the failed alert!'
        }
          success { 
            echo 'This run when pipeline success ,say success!'
        }

    }
}