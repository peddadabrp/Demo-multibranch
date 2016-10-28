node ('linux'){
   wrap([$class: 'TimestamperBuildWrapper']) {
    def mvnHome
    stage ('Clean workspace') {
       step([$class: 'WsCleanup'])
    }
    stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
       sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/Demo-multibranch.git"
       sh "mkdir preparation && cd preparation && ls -lart && pwd "
       sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/Demo-multibranch.git"
       sh "cp Jenkinsfile ../"
       sh "cd ../"
       sh "rm -rf preparation"
       sh "git status"
       sh "git checkout devel-1"
       sh "git add ."
       sh "git commit -m 'new commit'"
       sh "git push origin devel-1"
       sh "sleep 1"
       
    }
    
  }
   
}
