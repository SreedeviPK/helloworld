pipeline {
    agent any
    tools{
        maven "MAVENHOME"
    }
    environment {
        PATH = "/opt/apache-maven-3.6.3/bin:$PATH"
    }
    stages {
        stage("clone code"){
            steps{
               git url: 'https://github.com/SreedeviPK/helloworld.git'
            }
        }
        stage("build code"){
            steps{
              bat "mvn clean install"
            }
        }/*
        stage("deploy"){
            steps{
              sshagent(['deploy_user']) {
                 sh "scp -o StrictHostKeyChecking=no webapp/target/webapp.war ec2-user@13.229.183.126:/opt/apache-tomcat-8.5.55/webapps"
                 
                }
            }
        }*/
    }
}
