pipeline
{
    agent any
    tools
    {
        maven "maven 3.8.6"
    }
    stages
    {
        stage('Initialize')
        {
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
            }
        }
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
