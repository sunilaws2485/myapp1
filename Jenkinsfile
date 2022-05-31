pipeline {
    agent any

    environment{
        PATH ="/opt/apache-maven-3.5.3/bin:$PATH"

    }
    
    stages {
        stage('GIT CHECKOUT'){
            steps {
                git credentialsId: 'GITCREDS', url: 'https://github.com/sunilaws2485/myapp1'
            }
        }

        stage('MAVEN BUILD'){

            steps {
                sh "mvn clean package"
                sh "mv target/*.war target/myweb.war"
            }
        }     

        stage('Deploy'){

            steps {

                sshagent(['tomcat-creds1']) {
           
                    sh """

                       scp -o StrictHostKeyChecking=no  target/myweb.war  ec2-user@34.203.223.18:/opt/tomcat8/webapps/

                       ssh  ec2-user@34.203.223.18:/opt/tomcat8/bin/shutdown.sh
                       ssh  ec2-user@34.203.223.18:/opt/tomcat8/bin/startup.sh

                    """
                       }    
            }
        }         
        
    }
}