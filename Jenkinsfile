pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven3"
    }

    stages {
        stage('Github') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url: 'https://github.com/Satturi-Prashanth/java-shopping-project-tomcat.git'
            }
        }
        
        stage('Build') {
            steps {
                // Run Maven on a Unix agent.
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
} 
