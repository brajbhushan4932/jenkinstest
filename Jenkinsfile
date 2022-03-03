pipeline {

    agent any

    stages {

        stage('Build and Test') {

            steps {
                echo 'Building and Testing..'
            }
        }
    }

    post {
        success {
            echo "Pipeline SUCCESS..."
        }
    }
}
