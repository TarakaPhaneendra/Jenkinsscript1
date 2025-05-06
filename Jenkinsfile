pipeline {
    agent any

    tools {
        maven "MAVEN_HOME"  // Ensure this name matches the one configured in Jenkins global tools
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'naveenscript', url: 'https://github.com/TarakaPhaneendra/Jenkinsscript1.git'
               
            }
             post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }

       
    }

   
}
