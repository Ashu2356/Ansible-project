pipeline {
    agent any

    stages {
        stage('Clone Java Project') {
            steps {
                sh '''
                    git clone https://github.com/Ashu2356/Ansible-project.git project
                '''
            }
        }

        stage('Run Ansible for DEV') {
            steps {
                sh '''
                    ansible-playbook -i inventory/dev site.yml
                '''
            }
        }

        stage('Run Ansible for QA') {
            steps {
                sh '''
                    ansible-playbook -i inventory/qa site.yml
                '''
            }
        }
    }
}
