pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
            stage('Deploy the proxy') 
			{
                steps 
			{
                    sh "mvn install " +
                            "    -Pqa -Denv=${params.apigee_env} -Dorg=${params.apigee_org} " +
                            "    -Dusername=${params.apigee_user} " +
                            "    -Dpassword=${params.apigee_pwd}"
            }
        }
	}
}
