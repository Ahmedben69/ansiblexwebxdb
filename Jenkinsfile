pipeline {
    agent any
   
    stages {
        stage('SSH') { 
            steps {
                script{
                    node {
                       def remote = [:]
                       remote.name = 'fabio'
                       remote.host = '40.127.107.20'
                       remote.user = 'fabio'
                       remote.identityFile = '/home/fabio/.ssh/id_rsa.pub'
                       remote.allowAnyHosts = true
                       def secondRemote = [:]
                       secondRemote.name = 'fabio'
                       secondRemote.host = '4.233.106.239'
                       secondRemote.user = 'fabio'
                       remote.identityFile = '/home/fabio/.ssh/id_rsa.pub'
                       secondRemote.allowAnyHosts = true
                    }
                }
            }
        }
        stage ('Ansible-playbook') {
            steps {
                script {
                    sh "ansible-playbook playbook.yaml -i mon_inventaire.ini"
                }                
            }           
        }    
    }
}
