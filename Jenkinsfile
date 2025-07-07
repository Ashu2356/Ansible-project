pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/your-org/your-java-project.git'
            }
        }

        stage('Run Ansible') {
            steps {
                sh '''
                    cd ansible
                    ansible-playbook -i inventory/dev site.yml
                    ansible-playbook -i inventory/qa site.yml
                '''
            }
        }
    }
}

