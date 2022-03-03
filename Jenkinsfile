pipeline {
	triggers { pollSCM('H/10 * * * *') }
    // use the 'tools' section to use specific tool versions already defined in Jenkins config
    

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
