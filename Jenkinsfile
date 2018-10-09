pipeline {
   agent none
   stages {
     stage('build') {
       parallel {
        stage('CentOS7') {
           agent { dockerfile { filename 'centos7' dir '.dockerfiles' } }
           steps { sh 'cat /etc/os-release' }
        }
        stage('Debian8') {
           agent { dockerfile { filename 'debian8' dir '.dockerfiles' } }
           steps { sh 'cat /etc/os-release' }
        }
        stage('Debian9') {
          agent { dockerfile { filename 'debian9'  dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
        stage('ubuntu14.04') {
          agent { dockerfile { filename 'ubuntu14.04' dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
        stage('ubuntu16.04') {
          agent { dockerfile { filename 'ubuntu16.04' dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
       }
    }
  }
}
