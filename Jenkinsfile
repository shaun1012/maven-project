pipeline {
    agent any


    stages 
    {  
        
        stage ('SCM Checkout') {
          git 'https://github.com/shaun1012/maven-project.git'
         }
    
    }
    {
                            
        
        stage ('Testing Sstage') {


            steps {
                withMaven(maven : 'LocalMaven')
                {
                    sh 'mvn test'
                }
                  }
                                 
        }
		}
		}
