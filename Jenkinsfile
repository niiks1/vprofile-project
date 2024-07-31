pipeline {
    agent any
    tools {
        maven 'MAVEN3'
        jdk 'openjdk8'
    }
    environment {
        NEXUSIP ='172.31.28.15'
        NEXUSPORT ='8081'
        NEXUS_GRP_REPO ='vpro-maven-group'
        SNAP_REPO ='vprofile-snapshot'
        NEXUS_USER ='admin'
        NEXUS_PASS ='admin123'
        RELEASE_REPO ='vprofile-release'
        CENTRAL_REPO ='vprofile-maven-central'
        NEXUS_LOGIN ='nexuslogin'
    }

    stages {
        stage('Build') {
            steps{
                sh 'mvn -s settings.xml -DskipTests install'   
            }
        }
    }
}