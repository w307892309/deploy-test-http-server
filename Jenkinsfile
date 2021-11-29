pipeline {
    agent any

    stages {
        stage('ansible deploy') {
            steps {
                ansiblePlaybook {
                    credentialsId: 'site.shakhmin.ru', 
                    disableHostKeyChecking: true, 
                    installation: 'Ansible', 
                    inventory: 'site.shakhmin.ru,', 
                    playbook: 'playbook.yaml', 
                    vaultCredentialsId: 'ansible-vault'
                }
            }
        }
    }
}
