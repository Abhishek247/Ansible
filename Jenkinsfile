pipeline { 
   agent {label 'terraform'} 
    stages{
        stage('Clone Cookbook from Git') {
            steps {
		sh "cd $WORKSPACE"
                sh "git clone https://github.com/Abhishek247/Ansible.git"
		sh "ls -al"
            }
        }
        stage('Run Ansible Playbook') {
	    steps{
            	sh "ansible-playbook tomcat-setup.yml"
	    }
        }
    }
}
