pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
            ''' 
      }
    }
      stage ('Check-Git-Secrets') {
   steps {
    sh 'sudo su'
    sh 'rm trufflehog || true'
    sh 'docker run gesellix/trufflehog --json https://github.com/sindhuhack/snakegame-yoga.git > trufflehog'
    sh 'cat trufflehog'
   }
      }
  }
}
