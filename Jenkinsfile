pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build Code'
            }
        }
        
        stage('Test') {
            steps {
              echo  'Test Code'
             
               sh 'git --version'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy code'
            }
        }
    }
  
  post
  {
    always
    {
      emailext body: 'Summary of CI', subject: 'Pipeline Status', to: 'pratikshaasane9@gmail.com'
    }
  }
    
   
}
