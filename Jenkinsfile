pipeline
{
	agent any;
	stages
	{
		stage("Build")
		{
			step
			{
				sh "mvn clean package"
			}
		}
		stage("Create Tomcat Container and Deploy War to Tomcat Container")
		{
			step
			{
				sh "sudo docker image build -t tomcat:1.0 ."
				sh "sudo docker run -itdp 8081:8080 --name mytomcat tomcat:1.0"				
			}
		}
	}
}
