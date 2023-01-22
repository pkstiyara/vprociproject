pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment{
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin'
        RELEASE_REPO = 'vprofle-release'
        NEXUSIP = '172.31.12.161'
        NEXUSPORT = 8081
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXU_LOGIN = 'nexuslogin'
    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s setting.xml -DskipTests install'
            }
        }
    }
}