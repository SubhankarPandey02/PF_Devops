
pipeline {

    agent any

    parameters {
        choice(
            name: 'ACTION',
            choices: [
                'INSTALL',
                'START',
                'STOP',
                'HEALTHCHECK',
                'UNINSTALL'
            ],
            description: 'Select PingFederate action'
        )
    }

    stages {

        stage('Install') {
            when {
                expression { params.ACTION == 'INSTALL' }
            }
            steps {
                sh 'ansible-playbook -i inventory/hosts PF-NEW/pf-install.yml'
            }
        }

        stage('Start') {
            when {
                expression { params.ACTION == 'START' }
            }
            steps {
                sh 'ansible-playbook -i inventory/hosts PF-NEW/pf-start.yml'
            }
        }

        stage('Stop') {
            when {
                expression { params.ACTION == 'STOP' }
            }
            steps {
                sh 'ansible-playbook -i inventory/hosts PF-NEW/pf-stop.yml'
            }
        }

        stage('Health Check') {
            when {
                expression { params.ACTION == 'HEALTHCHECK' }
            }
            steps {
                sh 'ansible-playbook -i inventory/hosts PF-NEW/pf-health.yml'
            }
        }

        stage('Uninstall') {
            when {
                expression { params.ACTION == 'UNINSTALL' }
            }
            steps {
                sh 'ansible-playbook -i inventory/hosts PF-NEW/pf-uninstall.yml'
            }
        }
    }
}
