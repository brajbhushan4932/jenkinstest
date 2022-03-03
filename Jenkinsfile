pipeline {

    agent any

    stages {

        stage('Build and Test') {

            steps {
                echo 'Building and Testing..'
            }
        }
    }
    
    stages{
        stage("Docker login"){
            steps{
                sh 'aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 374263475486.dkr.ecr.ap-south-1.amazonaws.com'
                echo 'AWS Docker Login Success...'
            }
        }
   }
    
    //stage('Deploy'){
    //    steps{
    //        script{
     //           docker.withRegistry{
     //               'https://374263475486.dkr.ecr.ap-south-1.amazonaws.com',
     //                   'ecr:ap-south-1:my.aws.credentials'{
     //                       def myImage = docker.build('374263475486.dkr.ecr.ap-south-1.amazonaws.com/dev_mcip/test:test_tag')
      //                      myImage.push()
      //                  }
      //          }
      //      }
     //   }
   // }

    post {
        success {
            echo "Pipeline SUCCESS..."
        }
    }
}
