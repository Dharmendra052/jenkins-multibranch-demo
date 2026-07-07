pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to Dev') {
            when {
                branch 'dev'
            }
            steps {
                echo 'Deploying to Development'
            }
        }

        stage('Deploy to Production') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying to Production'
            }
        }
    }
}
