pipeline {
    agent any
    tools {
        maven 'Maven'
        nodejs 'NodeJS'
    }
    stages {
            stage('Deploy the proxy') 
			{
                steps 
			{
                    sh "mvn install " +
                            "    -Ptest -Denv=${params.apigee_env} -Dorg=${params.apigee_org} " +
                            "    -Dusername=${params.apigee_user} " +
                            "    -Dpassword=${params.apigee_pwd}"
            }
        }
	}
}