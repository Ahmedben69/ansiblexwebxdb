pipeline {
    agent any
   
    stages {
        stage ('Ansible-playbook') {
            steps {
                ansiblePlaybook credentialsId: 'fabio', disableHostKeyChecking: true, installation: 'ansible', inventory: '/var/lib/jenkins/workspace/ansiblexwebxdb/mon_inventaire.ini', playbook: '/var/lib/jenkins/workspace/ansiblexwebxdb/playbook.yaml'
            }           
        }    
    }
}
