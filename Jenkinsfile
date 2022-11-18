pipeline
{
	agent any
	stages
	{
		stage('Check-Out')
		{
			steps
			{
				checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/ck-g/New-Repo.git']]])
			}
		}
		stage('Build')
		{
			steps
			{
				withMaven(globalMavenSettingsConfig: 'null', jdk: 'JAVA_HOME', maven: 'M2_HOME', mavenOpts: 'clean package', mavenSettingsConfig: 'null') 
				{
    					
				}
			}
		}
	}
}
