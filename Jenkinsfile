pipeline{
    agent any
    tools{
        maven "MAVEN3"
        java "OracleJDK8"
    }
    environment{
        SNAP-REPO = 'vprofile-snapshot'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'admin'
        RELEASE-REPO = 'vprofle-release'
        NEXUSIP = '172.31.12.161'
        NEXUSPORT = 8081
        NEXUS-GRP-REPO = 'vpro-maven-group'
        NEXUS-LOGIN = 'nexuslogin'
    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s setting.xml -DskipTests install'
            }
        }
    }
}