pipeline {
    agent any

    tools {
        maven "MAVEN_HOME"  // This name must match what's set in Jenkins > Global Tool Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'naveenscript', url: 'https://github.com/TarakaPhaneendra/Jenkinsscript1.git'
            }
        }

     

        stage('Results') {
            steps {
                junit '**/target/surefire-reports/TEST-*.xml'
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
