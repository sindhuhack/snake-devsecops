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
//      stage ('Check-Git-Secrets') {
  // steps {
    //sh 'sudo su'
    //sh 'rm trufflehog || true'
    //sh 'sudo docker run gesellix/trufflehog --json https://github.com/sindhuhack/snakegame-yoga.git > trufflehog'
    //sh 'cat trufflehog'
   //}
     // }
         stage ('Nmap') {
      steps {
         sh 'sudo docker run instrumentisto/nmap -A -T4 192.168.1.1 > nmapresult'
        sh 'cat nmapresult'
      }
         }
    
        //stage ('Source Composition Analysis') {
      //steps {
        // sh 'rm owasp* || true'
         //sh 'wget "https://raw.githubusercontent.com/sindhuhack/snakegame-yoga/master/owasp-dependency-check.sh" '
         //sh 'chmod +x owasp-dependency-check.sh'
         //sh 'sudo bash owasp-dependency-check.sh'
         //sh 'cat /var/lib/jenkins/OWASP-Dependency-Check/reports/dependency-check-report.xml'
        
      //}
    //}
  }
}
