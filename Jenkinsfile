pipeline 
{
    agent any
	
     tools
	{
	maven "MAVEN_HOME"
	}

    stages 
	{
	        stage('Build') 
        	{
         		steps
          		{
			
			git 'https://github.com/ravikumarnk/test_jenkins1.git'
			//sh "mvn -Dmaven.test.failure.ignore=true clean package" 
                	 
          		}
        	}
          }

    post
    {
        always
        {
            	emailext body: 'here is th body', subject: 'error', to: 'ravikelakam@gmail.com'
		echo 'Deployment completed..  my app'
        }
        
    }
    
    
}
