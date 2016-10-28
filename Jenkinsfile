node ('linux'){
   wrap([$class: 'TimestamperBuildWrapper']) {
    def mvnHome
    stage ('Clean workspace') {
       step([$class: 'WsCleanup'])
    }
    stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
       //sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/Demo-multibranch.git"
       //sh "git clone https://github.com/peddadabrp/Demo-multibranch.git"
       checkout([$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/peddadabrp/sample-maven-project.git']]])
       //sh "ls -lart && mkdir preparation && cd preparation && ls -lart && pwd "
       //sh "git clone https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/multibranch-build-scripts.git"
       sh "git clone https://github.com/peddadabrp/multibranch-build-scripts.git"
       //sh "cd multibranch-build-scripts/"
       sh "ls -lart"
       sh "yes | cp -rf multibranch-build-scripts/Jenkinsfile ."
       //sh "cd ../"
       sh "ls -lart"
       sh "rm -rf multibranch-build-scripts"
       //sh "cd Demo-multibranch/"
       sh "ls -lart"
       sh "git status"
       sh 'git config --global user.name "peddadabrp"'
       sh "git config --global user.email rajendra.peddada@infostretch.com"
       //sh "git checkout devel-1"
       sh "git branch -all"
       sh "git checkout master"
       sh "git add ."
       sh "git commit -m 'new commit'"
       //sh 'git pull --all'
       //sh "git remote add origin git@github.com:peddadabrp/sample-maven-project.git"
       //sh "git push --repo https://peddadabrp:chinnuchinnu07@github.com/peddadabrp/sample-maven-project.git --all"
       //sh "git push -u --all"
       sh "git push origin --all"
       sh "sleep 1"
       
    }
    step([$class: 'WsCleanup'])
  }
   
}
