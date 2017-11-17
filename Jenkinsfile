pipeline {
  agent any
  stages {
    stage('master') {
      parallel {
        stage('master') {
          steps {
            git(url: 'https://github.com/Imransysg/example-voting-app.git', branch: 'master', changelog: true, credentialsId: 'im-git', poll: true)
          }
        }
        stage('Vote Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def vote_img = docker.build('dockeradmin/voting-app-vote','./vote').push('latest')
                }
              }
            }
            
          }
        }
        stage('Worker Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  // dtr-login is a login ID in credentials
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def worker_img = docker.build('dockeradmin/voting-app-worker','./worker').push('latest')
                }
                
              }
            }
            
          }
        }
        stage('Result Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def result_img = docker.build('dockeradmin/voting-app-result','./result').push('latest')
                  
                }
              }
            }
            
          }
        }
      }
    }
    stage('alpha') {
      parallel {
        stage('alpha') {
          steps {
            git(url: 'https://github.com/Imransysg/example-voting-app.git', branch: 'alpha', changelog: true, credentialsId: 'im-git', poll: true)
          }
        }
        stage('Vote Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def vote_img = docker.build('dockeradmin/voting-app-vote','./vote').push('latest')
                }
              }
            }
            
          }
        }
        stage('Worker Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  // dtr-login is a login ID in credentials
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def worker_img = docker.build('dockeradmin/voting-app-worker','./worker').push('latest')
                }
                
              }
            }
            
          }
        }
        stage('Result Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def result_img = docker.build('dockeradmin/voting-app-result','./result').push('latest')
                  
                }
              }
            }
            
          }
        }
      }
    }
    stage('stg') {
      parallel {
        stage('stg') {
          steps {
            git(url: 'https://github.com/Imransysg/example-voting-app.git', branch: 'stg', changelog: true, credentialsId: 'im-git', poll: true)
          }
        }
        stage('Vote Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def vote_img = docker.build('dockeradmin/voting-app-vote','./vote').push('latest')
                }
              }
            }
            
          }
        }
        stage('Worker Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  // dtr-login is a login ID in credentials
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def worker_img = docker.build('dockeradmin/voting-app-worker','./worker').push('latest')
                }
                
              }
            }
            
          }
        }
        stage('Result Image') {
          steps {
            script {
              node
              {
                docker.withRegistry('https://meet.lync.com/sysgain365/rrai/HN15Y799','dtr-login'){
                  git 'https://github.com/Imransysg/example-voting-app.git/'
                  def result_img = docker.build('dockeradmin/voting-app-result','./result').push('latest')
                  
                }
              }
            }
            
          }
        }
      }
    }
  }
}
