node {

    stage('SCM checkout'){
       git 'https://github.com/sunilaws2485/myapp1'
       }

    stage('compile-package'){
        // Get maven home path
       def mvnHOME = tool name: 'maven3', type: 'maven'
       sh "${mvnHOME}/bin/mvn package"
       }

    stage('EMAIL-NOTIFICATION'){
        mail bcc: '', body: '''Hi team

        Build completed''', cc: '', from: '', replyTo: '', subject: 'Jenkinsbuild-Alert', to: 'sunilaws2485@gmail.com'

    }

}