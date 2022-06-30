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
    }
}
