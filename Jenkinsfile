pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/<your-username>/my-cicd-project.git'
            }
        }

        stage('Run Ansible') {
            steps {
                ansiblePlaybook(
                    playbook: 'ansible/deploy.yaml',
                    inventory: 'inventory'
                )
            }
        }
    }
}
