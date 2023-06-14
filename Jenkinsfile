pipeline {
    agent any
   
    stages {
        stage('SSH') {
           steps {
               script{
                   node {
                       def remote = [:]
                       remote.name = 'fabio1'
                       remote.host = '20.43.59.103'
                       remote.user = 'fabio'
                       remote.password = 'Dofus69200Fabio'
                       remote.allowAnyHosts = true
                       def secondRemote = [:]
                       secondRemote.name = 'fabio2'
                       secondRemote.host = '4.233.106.239'
                       secondRemote.user = 'fabio'
                       secondRemote.password = 'Dofus69200Fabioa'
                       secondRemote.allowAnyHosts = true
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
