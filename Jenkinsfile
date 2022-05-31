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
        
    }
}