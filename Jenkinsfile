pipeline {
    agent any

    stages {

        stage('Setup') {
            steps {
                sh 'pip install pandas scikit-learn'
            }
        }

        stage('Train') {
            steps {
                sh 'python train.py'
            }
        }

        stage('Identity') {
            steps {
                echo 'Name  : Balagopal'
                echo 'Roll  : 2022BCS0058'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'model.pkl, metrics.json', fingerprint: true
            }
        }

    }
}
