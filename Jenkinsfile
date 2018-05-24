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
		withCredentials([usernamePassword(credentialsId: 'apigeeCreds', usernameVariable: 'apigee_user', passwordVariable: 'apigee_pwd')]) {
                    bat "mvn install " +
                            "    -Pqa -Denv=${params.apigee_env} -Dorg=${params.apigee_org} " +
                            "    -Dusername=$apigee_user " +
                            "    -Dpassword=$apigee_pwd"
		}
            }
        }
	}
}
