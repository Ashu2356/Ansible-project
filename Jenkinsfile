pipeline {
    agent any

    stages {
        stage('Clone Java Project') {
            steps {
                sh '''
                    rm -rf project 
                    git clone https://github.com/Ashu2356/project.git
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
