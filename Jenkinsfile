pipeline {
  agent any
  stages {
           
        stage('alpha') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://10.1.53.13/','dtr-login'){
                  // dtr-login is a login ID in credentials
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  
                }
                
              }
            }
            
          }
        }
      }
    }
 
