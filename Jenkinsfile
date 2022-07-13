pipeline {
    agent any
    parameters {
            string(name: 'Name', description: 'Please enter your name')
            choice(name: 'Technology', choices: ['Python','Java'], description: 'Choose Technology')
           }

    stages {
        stage('Build') {
            steps {
                echo 'Build Code'
            }
        }

        stage('Test') {
            steps {
              echo  'Test Code'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy code'
            }
        }
        
        stage ('Printing information') {
        steps {
           script {
               def name = "${params.Name}"
               def tech = "${params.Technology}"
               if(tech == "Python")
                 {
                  echo "Welcome to Python programming Language"
                 } 
               
               else
                 {
                  echo "Welcome to Java programming Language"
                 } 
               } 
             }
           }
    }

  post
  {
    always
    {
      emailext body: 'Summary of CI', subject: 'Pipeline Status', to: 'nitishy.08@gmail.com'
    }
  }

}
