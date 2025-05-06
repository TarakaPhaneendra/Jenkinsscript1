pipeline {
    agent any

    tools {
        maven "MAVEN_HOME"  // Ensure this name matches the one configured in Jenkins global tools
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'naveenscript', url: 'https://github.com/TarakaPhaneendra/Jenkinsscript1.git'
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }

       
    }

   
}
