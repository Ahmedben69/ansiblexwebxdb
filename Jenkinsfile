pipeline {
    agent any
   
    stages {
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
