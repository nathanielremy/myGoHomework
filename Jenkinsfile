pipeline{
    agent any
    tools {
        go {'go'}
        }

    stages {
        stage('Build') { 
            steps{
                sh 'go build'
            }
        }        
        stage('Publish artefact') {
            steps{
                archiveArtifacts 'go_build'
            }
        }
    }
}