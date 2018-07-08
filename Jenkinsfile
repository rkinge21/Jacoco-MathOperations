pipeline
{
	agent any
	stages
	{
		stage('Clean Install Stage')
		{
			steps
			{
				withMaven(maven : 'maven3_5_3')
				{
			   	   bat 'mvn clean install'
			   	}
			}
		}
		stage('Testing Stage')
		{
			steps
			{
				withMaven(maven : 'maven3_5_3')
				{
				   bat 'mvn test'
				}
			}
		}
	}
}
