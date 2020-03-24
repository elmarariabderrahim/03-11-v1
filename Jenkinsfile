pipeline {
    agent any 
    stages {
        stage('generate_DDL') {
            steps {
		    
		 
        	    bat 'exp_script.sh'
		   
		    
            }
        }
        stage('Import_schema_apply_scripts') {
            steps {
		    bat 'docker start test-mysql' 
		    
        	    bat 'add_to_container.sh'            }
        }
        stage('Apply_to_db') {
            steps {
		    
		   
        	    bat 'apply_scripts_db.sh'  
            }
        }
    }
}
