pipeline {
    agent any
   
    stages {
        stage('SSH') { 
            steps {
                script{
                    node {
                       def remote = [:]
                       remote.name = 'fabio'
                       remote.host = '20.43.59.103'
                       remote.user = 'fabio'
                       remote.identityFile = '~/.ssh/id_rsa'
                       remote.allowAnyHosts = true
                    }
                }
            }
        }
            
        stage ('Ansible-playbook') {
            steps {
                script {
                    sh "ansible -i mon_inventaire.ini -m ping all"
                    sh "ansible-playbook playbook.yaml -i mon_inventaire.ini"
                }                
            }           
        }    
    }
}
