pipeline {
    agent {
        node {
            label 'AGENT-1'
            
        }
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
                echo "Deploy..."
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