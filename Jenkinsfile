node ('linux'){
   wrap([$class: 'TimestamperBuildWrapper']) {
    def mvnHome
    stage ('Clean workspace') {
       step([$class: 'WsCleanup'])
    }
    stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
       checkout scm
       sh "mkdir preparation && cd preparation"
       checkout([$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/peddadabrp/Demo-multibranch.git']]])
       sh "cp Jenkinsfile ../"
       sh "rm -rf preparation"
       sh "sleep 1"
       
    }
    
  }
   
}
