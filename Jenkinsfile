pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/BoukhrissM/spring-jenkins.git'
            }
        }

        stage('Build') {
                steps {
                    // To run Maven on a Windows agent, use
                    bat "mvn -Dmaven.test.failure.ignore=true clean package"
                }
        }

        stage('Copy') {
                        steps {
                            // To run Maven on a Windows agent, use
                            bat "copy target\\jenkinsTPspring-0.0.1-SNAPSHOT.jar C:\\Users\\bouuk\\Desktop\\cours\\jenkinsTp\\deploy\\jenkinsTPspring-0.0.1-SNAPSHOT.jar"
                        }
        }
    }
}
