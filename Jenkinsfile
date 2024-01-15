
pipeline 
{
    agent any

    stages 
	{
	       	stage('Test') 
        	{
         		steps
          		{
			clean test	
                	echo 'Testing my app'
          		}
        	}
	
		stage('Build') 
        	{
         		steps
          		{
			verify				
                	echo 'Building my app'
          		}
        	}

		stage('install') 
        	{
         		steps
          		{
			install
                	echo 'Deploy my app'
          		}
        	}
        	
    }
    post
    {
        always
        {
            	emailext body: 'here is th body', subject: 'CICD info', to: 'ravikelakam@gmail.com'
		echo 'Deployment completed..  my app'
        }
        
    }
    
    
}
