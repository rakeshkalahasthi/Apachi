pipeline {
    
    agent any


    tools {
    jdk 'Java'
    maven 'Maven'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
               git branch: 'main',
               url: 'https://github.com/chinni4321/apache2.git'
            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd $WORKSPACE
                  aws s3 sync . s3://demo15545
                  '''

            }
        }
      }
     }
