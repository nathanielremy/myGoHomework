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
                archiveArtifacts 'myGo2HWmoms_master'
            }
        }
    }
}