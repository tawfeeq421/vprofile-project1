pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK11"
    }
    
    environment {
        SNAP_REPO = 'fsa2'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'admin123'
		RELEASE_REPO = 'fsa'
		CENTRAL_REPO = 'fsa-pro'
		NEXUSIP = '172.31.88.38'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'fsa-rep-gr'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
