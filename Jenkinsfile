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
        }

       
    }

    post {
        always {
            // Publish test results even if some tests failed
            junit '**/target/surefire-reports/*.xml'
            // Archive built JAR (if created)
            archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
        }
    }
}
