pipeline {

    agent any

    stages {

        stage('Debug') {
            steps {
                sh '''
                pwd
                ls -la
                find . -type f
                '''
            }
        }

    }
}
