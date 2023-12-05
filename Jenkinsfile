pipeline {
    agent any
    
    stages {
        stage('Run Katalon Tests') {
            steps {
                script {
                    // Run Katalon Studio tests using Docker
                    sh 'docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -retry=0 -testSuitePath="Test Suites/Suite1" -browserType="Chrome" -executionProfile="default" -apiKey="3315bf05-eb56-4f10-8716-6762fb652ee4"'
                }
            }
        }
    }
}

