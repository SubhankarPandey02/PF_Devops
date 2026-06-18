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
                sh 'ansible-playbook /home/subhankar/pf-devops/playbooks/pf-health.yml'
            }
        }

    }
}
