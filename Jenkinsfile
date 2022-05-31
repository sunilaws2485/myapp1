

   properties([parameters([choice(choices: 'master\nfeature-1\nfeature-2', name: 'branch')])])

   node{

   

      stage('SCM CHECKOUT'){

        echo "pull the code from branch : "${params.branch}" 
        git url: 'https://github.com/sunilaws2485/myapp1', branch: "${params.branch}"

    }




}