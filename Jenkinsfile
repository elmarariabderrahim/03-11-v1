pipeline {
    agent any 
    stages {
        stage('generate_DDL') {
            steps {
		    
		    bat 'chmod 777 ./exp_script.sh'
        	    bat './exp_script.sh'
		   
		    
            }
        }
        stage('Import_schema_apply_scripts') {
            steps {
		    bat 'docker start test-mysql' 
		    bat 'chmod 777 ./add_to_container.sh'
        	    bat './add_to_container.sh'            }
        }
        stage('Apply_to_db') {
            steps {
		    
		    bat 'chmod 777 ./apply_scripts_db.sh'
        	    bat './apply_scripts_db.sh'  
            }
        }
    }
}
