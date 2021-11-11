pipeline
{
    agent any
    stages
    {
        stage('scm checkout')
        {
            steps{
                git branch: 'master', url: 'https://github.com/Ranvijay7492/gradle-calculator'
            }
        }
        stage('code build')
        {
            steps{
                withGradle 
                {
                   sh './gradlew clean build'
                   sh './gradlew jar'
            }
            }
        }
        stage('code build')
        {
            steps{
                withGradle 
                {
                   sh './gradlew test'
            }
            }
        }
    }
}