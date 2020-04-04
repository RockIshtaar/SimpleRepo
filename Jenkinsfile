pipeline {
	agent any 
	
	stages {
		stage ('Copying Repository') {
			steps {
				echo '************************************************'
				echo 'Copying Files to Jenkins Server'
				git clone https://github.com/RockIshtaar/SimpleRepo.git
				echo '************************************************'
			}
		}
		stage ('Ansible Build') {
			steps{
				echo '************************************************'
				echo 'Running Ansible'
				sh label: '', script: 'sudo ansible-playbook -i hosts playbook1.yml'
				echo '************************************************'
			}
		}
		
	}
}
