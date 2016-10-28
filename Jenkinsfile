node ('linux'){
   wrap([$class: 'TimestamperBuildWrapper']) {
    def mvnHome
    stage ('Clean workspace') {
       step([$class: 'WsCleanup'])
    }
    stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
       sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/Demo-multibranch.git"
       sh "mkdir preparation && cd preparation"
       sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/Demo-multibranch.git"
       sh "cp Jenkinsfile ../"
       sh "cd ../"
       sh "git status"
       sh "git checkout devel-1"
       sh "git add ."
       sh "git commit -m 'new commit'"
       sh "git push origin devel-1"
       sh "rm -rf preparation"
       sh "sleep 1"
       
    }
    
  }
   
}
