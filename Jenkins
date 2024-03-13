pipeline {
  agent any 
  stages {
//   stage('Clone repository') {
//      steps {
//        checkout ([$class: 'GitSCM', 
//        branches: [[name: '*/main']], 
//        userRemoteConfigs: [[url: 'https://github.com/Rev-x/pes2ug21cs624_jenkins_']]})
//        }
//   }
      stage( 'Build') {
        steps {
          build 'pes2ug21cs620-1'
          sh 'g++ main.cpp -o output'
      }
    }
      stage ('Test') {
        steps {
          sh './output'
      }
    }
      stage ('Deploy') {
        steps {
          echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
