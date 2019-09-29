pipeline 
{
    agent any


    stages 
    {  
        stage ('SCM Checkout') 
	    {
         git 'https://github.com/shaun1012/maven-project.git'
     	    }
    
 }
	
   {
      stage ('Testing Sstage') 
	   {
	steps {
                withMaven(maven : 'LocalMaven')
                {
                    sh 'mvn test'
                }
                  }
                                 
        }
		}
	
	{
		stage('Deploy to Tomcat'){

steps {
  sshagent (['172.31.35.181']) {
    sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.35.181:/var/lib/tomcat/webapps'
  }
}
}
}
}
