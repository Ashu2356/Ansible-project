pipeline {
    agent any

    stages {
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
