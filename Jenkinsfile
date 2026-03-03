pipeline {
    agent any

    stages {

        stage('Build & Deploy') {
            steps {
                sh '''
                    cd /project
                    git reset --hard
                    git pull origin main
                    docker compose down
                    docker compose up -d --build
                '''
            }
        }

    }
}