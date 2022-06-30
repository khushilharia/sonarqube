pipeline
{
    agent any
    tools
    {
        maven 'maven 3.8.6'
    }
    stages
    {
        stage("GITHUB CHECKOUT")
        {
            steps
            {
                git branch: 'main', url: 'https://github.com/khushilharia/sonarqube.git'
                echo "Git Checkout Successful"
            }
        }
        stage("BUILD CHECKOUT")
        {
            steps
            {
                echo "Build Stage"
                bat 'mvn clean package'
                echo 'Maven step finished'
            }
        }
        stage('SonarQube analysis') 
        {
            //def scannerHome = tool 'SonarScanner 4.0';
            steps
            {
                withSonarQubeEnv('SonarQube 9.4.0') 
                { 
                    //If you have configured more than one global server connection, you can specify its name
                   //sh "${scannerHome}/bin/sonar-scanner"
                    bat "mvn sonar:sonar"
                }
            }
        }
    }
}
