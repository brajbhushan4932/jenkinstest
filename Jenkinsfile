pipeline {

    agent any

    stages {

        stage('Build and Test') {

            steps {
                echo 'Building and Testing..'
            }
        }
    }
    
    stage('Deploy'){
        steps{
            script{
                docker.withRegistry{
                    'https://374263475486.dkr.ecr.ap-south-1.amazonaws.com',
                        'ecr:ap-south-1:my.aws.credentials'{
                            def myImage = docker.build('374263475486.dkr.ecr.ap-south-1.amazonaws.com/dev_mcip/test:test_tag')
                            myImage.push()
                        }
                }
            }
        }
    }

    post {
        success {
            echo "Pipeline SUCCESS..."
        }
    }
}
