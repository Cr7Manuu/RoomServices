pipeline{
        agent any
        stages{
            stage('SonarQube analysis'){
            steps{
            withSonarQubeEnv('sonarcicd')
            {
            bat "mvn sonar:sonar"
            }
            }
        }
}
