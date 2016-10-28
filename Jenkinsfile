node ('linux'){
   wrap([$class: 'TimestamperBuildWrapper']) {
    def mvnHome
    stage ('Clean workspace') {
       step([$class: 'WsCleanup'])
    }
    stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
       //sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/Demo-multibranch.git"
       sh "git clone https://github.com/peddadabrp/Demo-multibranch.git"
       //sh "ls -lart && mkdir preparation && cd preparation && ls -lart && pwd "
       //sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/multibranch-build-scripts.git"
       sh "git clone https://github.com/peddadabrp/multibranch-build-scripts.git"
       sh "ls -lart && cd multibranch-build-scripts && yes | cp -rf Jenkinsfile ../Demo-multibranch/"
       sh "cd ../"
       sh "ls -lart && rm -rf preparation && cd Demo-multibranch && ls -lart"
       sh "git status"
       sh "git checkout devel-1"
       sh "git add ."
       sh "git commit -m 'new commit'"
       sh "git push origin devel-1"
       sh "sleep 1"
       
    }
    step([$class: 'WsCleanup'])
  }
   
}
