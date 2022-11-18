pipeline
{
	agent any
	stages
	{
		stage('Build')
		{
			steps
			{
				script
				{
					sh "mvn clean package"
				}
			}
		}
		stage('Create Tomcat Container and Deploy War to Tomcat Container')
		{
			steps
			{
				script
				{
					sh "sudo docker image build -t tomcat:1.0 ."
					sh "sudo docker run -itdp 8081:8080 --name mytomcat tomcat:1.0"	
				}
			}
		}
	}
}
