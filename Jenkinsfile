pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP_REPO = 'vprofile-snapshot'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_IP = '10.0.1.181'
        NEXUS_PORT = '8081'
        NEXUS_LOGIN = 'nexuslogin'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'platter-oozy-tibetan'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
