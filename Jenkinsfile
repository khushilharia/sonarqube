pipeline
{
    agent any
    tools
    {
        maven "Maven"
    }
    stages
    {
       stage('GetCode')
       {
            steps
            {
                git 'https://github.com/khushilharia/SonarqubeDemo.git/'
                echo "Git checkout successful"
            }
         }        
       stage('Build')
       {
            steps
            {
             	echo "Build Stage"
                sh 'mvn clean compile'
            }
         }
    }
}
