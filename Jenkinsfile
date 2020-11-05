pipeline {
    agent any
    stages {
        stage('git clone') {
            steps{  
                git branch: 'main', 
                    url: 'https://github.com/wahaj123/Ansible-wordpress.git'          
            }
        }
        stage('Ansible deploy') {          
            steps{
                ansiblePlaybook ( disableHostKeyChecking: true,
                                credentialsId: 'Wahaj-ohio', 
                                installation: 'Ansible', 
                                inventory: 'inventory/dev', 
                                playbook: 'playbook.yml',
                                vaultCredentialsId: 'dev')
            }
        }
    }
}