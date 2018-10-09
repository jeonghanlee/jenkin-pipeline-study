pipeline {
   agent none
   stages {
      parallel {
      stage('CentOS7') {
        agent {
	   dockerfile {
              filename 'centos7.dockerfile'
	      dir '.dockerfiles'
      	   }	      
        }
        steps {
          sh 'cat /etc/os-release'
        }
      }
      stage('Debian9') {
        agent {
	   dockerfile {
              filename 'debian9.dockerfile'
	      dir '.dockerfiles'
      	   }	      
        }
	steps {
	  sh 'cat /etc/os-release'
	}
     }
   }
   }
} 
