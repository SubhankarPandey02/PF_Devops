pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Run Ansible') {
            steps {
                sh 'ansible-playbook playbooks/pf-health.yml'
            }
        }

    }
}
