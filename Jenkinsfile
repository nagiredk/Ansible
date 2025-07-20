pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/nagiredk/Ansible.git'
            }
        }

        stage('Run install-ansible.sh') {
            steps {
                sh '''
                    chmod +x scripts/install-ansible.sh
                    echo "<your_password>" | sudo -S ./scripts/install-ansible.sh
                '''
            }
        }

        stage('Check Ansible version') {
            steps {
                sh '''
                    ansible --version
                '''
            }
        }
    }
}
