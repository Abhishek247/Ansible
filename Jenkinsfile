pipeline { 
   agent {label 'Ansible'} 
    stages{
        stage('Clone Cookbook from Git') {
            steps {
			    sh "cd $WORKSPACE"
                sh "git clone https://github.com/Abhishek247/Ansible.git"
		        sh "ls -al"
            }
        }
        stage('Run Ansible Playbook') {
            sh "ansible-playbook tomcat-setup.yml"
        }
    }
}
