pipeline {

stage('SCM checkout') {
    git 'https://github.com/sunilaws2485/myapp1'
}

stage('compile-package') {

   def mvnHOME = tool name: 'maven3', type: 'maven'
   sh "${mvnHOME}/bin/mvn package"

}

}