node {

   properties([parameters([choice(choices: ['master', 'feature-1', 'feature-2'], name: 'branch')])])

    stage('SCM CHECKOUT'){

        echo "pull the code from branch : "${params.branch}
        git url: 'https://github.com/sunilaws2485/myapp1', branch: "${params.branch}"

    }




}