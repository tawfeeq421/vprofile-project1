pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    
    environment {
        SNAP_REPO = 'maven-snap'
		NEXUS_USER = 'nexus'
		NEXUS_PASS = 'admin123'
		RELEASE_REPO = 'maven'
		CENTRAL_REPO = 'maven2'
		NEXUSIP = '172.31.91.59'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'maven-group'
        NEXUS_LOGIN = 'admin123'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
