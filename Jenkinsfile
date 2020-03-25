pipeline {
    agent any 
    stages {
        stage('generate_DDL') {
            steps {
		    
        	     bat 'sh -c ./exp_script.sh'
		   
		    
            }
        }
        stage('Import_schema_apply_scripts') {
            steps {
		    bat 'sh -c docker start test-mysql' 
        	   bat 'sh -c ./add_to_container.sh'            }
        }
        stage('Apply_to_db') {
            steps {
		    
        	    bat 'sh -c ./apply_scripts_db.sh'  
            }
        }
    }
}
