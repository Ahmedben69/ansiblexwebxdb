pipeline {
    agent any
   
    stages {
        
        stage ('Ansible-playbook') {
            steps {
                script {
                    sh "ansible-playbook playbook.yaml -i mon_inventaire.ini"
                }                
            }
        }   
    }    
}
