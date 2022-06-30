pipeline
{
    agent any
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
             	echo "Build Stage"
            }
         }
    }
}
