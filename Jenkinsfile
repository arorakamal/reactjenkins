pipeline {
  agent any
   stages{
    stage('SonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=arorakamal_reactjenkins -Dsonar.organization=arorakamal -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=ce5056eb245049dd528994206b023e6cec243cb5'
			}
        }
    }
}
