pipeline
{
    agent any
    environment
    {
        PATH="C:/Users/khush/Downloads/apache-maven-3.8.5-bin/apache-maven-3.8.5/bin/"
    }
    stages
    {
       stage('GetCode')
       {
            steps
            {
                git 'https://github.com/khushilharia/SonarqubeDemo.git/'
            }
         }        
       stage('Build')
       {
            steps
            {
             sh "mvn clean package"
            }
         }
        stage('SonarQube analysis') 
        {
        //  def scannerHome = tool 'SonarScanner 4.0';
			steps
			{
				withSonarQubeEnv('SonarQube 9.4.0') 
				{ 
				// If you have configured more than one global server connection, you can specify its name
				//  sh "${scannerHome}/bin/sonar-scanner"
					sh "mvn sonar:sonar"
				}
			}
       
		}
    }
}