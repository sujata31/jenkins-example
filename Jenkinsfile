pipeline {
    agent any
    
    stages {
	    
    stage('scm checkout'){
		   git 'https://github.com/sujata31/jenkins-example.git'	
              		
		}

    
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'my maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'my maven') {
                    sh 'mvn test'
                }
            }
        }


       // stage ('Deployment Stage') {
          //  steps {
             //   withMaven(maven : 'my maven') {
                //    sh 'mvn deploy'
               // }
           // }
        //}
    }
}
