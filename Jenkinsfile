pipeline {
    agent any

    stages {
        stage('PingFederate Health Check') {
            steps {
                sh '''
                pwd
                cat inventory/hosts
                ansible-playbook -i inventory/hosts playbooks/pf-health.yml
                '''
            }
        }
    }
}
