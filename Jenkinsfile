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
    stages {
      stage ('Check-Git-Secrets') {
   steps {
    sh 'rm trufflehog || true'
    sh 'docker run gesellix/trufflehog --json https://github.com/sindhuhack/Devsecops.git > trufflehog'
    sh 'cat trufflehog'
   }
    })
  }
}
