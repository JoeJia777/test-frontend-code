pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'yarn build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'yarn test'
            }
        }
        stage('Manual Check') {
            steps {
                input message: 'Are you sure to deploy? (Click "Yes" to continue)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
