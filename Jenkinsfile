pipeline{
    agent any
    tools {
        go {'go-1.14'}
        }

    stages {
        stage('Build') { 
            steps{
                sh 'go build'
            }
        }        
        stage('Publish artifact') {
            steps{
                copyArtifacts filter: 'myGo2HWmoms_master', fingerprintArtifacts: true, projectName: 'myGo2HWmoms', selector: lastSuccessful()
            }
        }
    }
}
