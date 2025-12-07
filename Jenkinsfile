pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/mehwish21-hub/jenkins-lab.git'
            }
        }
        stage('Run Ansible') {
            steps {
                sh 'ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i "192.168.43.129," deploy.yml --user mmvm2'
            }
        }
    }
}
