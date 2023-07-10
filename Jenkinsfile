 pipeline {
    agent any

    stages {
        stage('Build Docker image') {
            steps {
                script {
                    docker.withRegistry('766480565836.dkr.ecr.us-east-1.amazonaws.com/app
', 'Docker') {
                        def customImage = docker.build('app')
                        customImage.push('v1')
                    }
                }
            }
        }
    }
}