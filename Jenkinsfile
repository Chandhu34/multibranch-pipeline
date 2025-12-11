pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t image1 .'
            }
        }
        stage ("Tag") {
            steps {
                sh 'docker tag image1 chandu34/paytm:bank'
            }
        }
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bank-app -p 1111:80 chandu34/paytm:bank'
            }
        }
    }
}
