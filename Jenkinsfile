pipeline {
    agent any
    
    stages {
        stage('Pull Katalon Docker Image') {
            steps {
                script {
                    // Define the workspace directory
                    def workspace = pwd()
                    
                    // Pull Katalon Docker image into the workspace directory
                    sh "docker pull katalonstudio/katalon:latest"
                    sh "docker run -v ${workspace}:/katalon/katalon_execute -t katalonstudio/katalon:latest"
                }
            }
        }
    }
}
