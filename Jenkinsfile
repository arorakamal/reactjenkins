pipeline {
  agent any
  tools { 
        nodejs 'node'  
    }
   stages{
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm run build'
      }
    }
    stage('SonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=arorakamal_reactjenkins -Dsonar.organization=arorakamal -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=ce5056eb245049dd528994206b023e6cec243cb5'
			}
        }
        
    // stage('SnykAnalysis') {
    //         steps {		
		// 		withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
		// 			sh 'mvn snyk:test -fn'
		// 		}
		// 	} 
    //    }
     }
}
