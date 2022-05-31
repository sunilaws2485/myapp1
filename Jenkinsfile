
properties([parameters([choice(choices: ['master', 'feature-1', 'feature-2'], description: 'select the branch to build', name: 'branch')])])

node{

  stage('SCM CHECKOUT'){
       echo "pull the code from branch : ${params.branch}" 
        git url: 'https://github.com/sunilaws2485/myapp1', branch: "${params.branch}"

  }

}