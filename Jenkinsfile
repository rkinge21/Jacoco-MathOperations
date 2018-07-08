pipeline
{
	agent any
	stages
	{
		stage('Compile Stage')
		{
			steps
			{
				withMaven(maven : 'maven3_5_3')
				{
			   	   bat 'mvn clean compile'
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
		stage('Jacoco Collect')
		{
			steps
			{
				jacoco()
			}
		}
	}
}
