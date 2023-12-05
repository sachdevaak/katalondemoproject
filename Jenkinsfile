pipeline {
    agent any
    
    stages {
        stage('Run Katalon Tests') {
            steps {
                script {
                    // Run Katalon Studio tests using Docker
                     sh 'docker run -t --rm -v "/var/jenkins_home/5_KatalonTestDocker":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/Users/Akhil/Katalon Studio/DemoProject1 -retry=0 -testSuitePath="Test Suites/Suite1" -browserType="Chrome" -executionProfile="default" -apiKey="6052bbfe-f4fc-4553-b334-6769d9eff78b"'
                }
            }
        }
    }
}

