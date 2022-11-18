pipeline
{
	agent
	{
		label 
		{
			label 'Master'
			customWorkspace '/opt/Jenkins-Master'
		}
	}
	stages
	{
		stage('checkout')
		{
			steps
			{
				sh '''
					rm -fr *
					git init
					git clone https://github.com/ck-g/New-Repo.git .					
					mvn clean package					
				'''
			}
		}	
	}
}
