	 {
	 agent any 
         parameters {
            string(name: 'Name', description: 'Please enter your name')
            choice(name: 'Technology', choices: ['Python','Java'], description: 'Choose Technology')
           }

	 stages {
	     stage ('Printing information')
        {
        steps {
           script {
               def name = "${params.Name}"
               def tech = "${params.Technology}"
               if(tech == "Python")
                 {
                  echo "Welcome to Python programming Language
                } 
               
               else
                 {
                  echo "Welcome to Java programming Language
                } 
              } 
            
              }
           }
         }
       }
