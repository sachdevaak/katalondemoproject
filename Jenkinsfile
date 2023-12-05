pipeline {
    agent any
    
    stages {
        stage('Run Katalon Tests') {
            steps {
                script {
                    // Run Katalon Studio tests using Docker within Jenkins pipeline
                    docker.image('katalonstudio/katalon')
                        .inside('-v /var/jenkins_home/workspace/5_KatalonTestDocker:/tmp/project') {
                            sh "katalonc.sh -projectPath=/tmp/project -retry=0 -testSuitePath='Test Suites/Suite1' -browserType='Chrome' -executionProfile='default' -apiKey='6052bbfe-f4fc-4553-b334-6769d9eff78b'"
                        }
                }
            }
        }
    }
}

