pipeline {
   agent none
   stages {
     stage('build') {
       parallel {
        stage('CentOS7') {
           agent { dockerfile { filename 'centos7.dockerfile'
           dir '.dockerfiles' } }
           steps {
             sh 'cat /etc/os-release'
	           sh 'git clone https://github.com/icshwi/e3'
             sh 'cd e3'
             sh 'bash e3_builder_conf.bash -b "3.15.5" -t "${HOME}/epics" setup'
             sh 'bash e3.bash base "y"'
          }      
        }
        stage('Fedora28') {
           agent { dockerfile { filename 'fedora28.dockerfile'
           dir '.dockerfiles' } }
           steps { sh 'cat /etc/os-release' }
        }
        stage('Debian8') {
           agent { dockerfile { filename 'debian8.dockerfile'
           dir '.dockerfiles' } }
           steps { sh 'cat /etc/os-release' }
        }
        stage('Debian9') {
          agent { dockerfile { filename 'debian9.dockerfile'
          dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
        stage('Debian10') {
          agent { dockerfile { filename 'debian10.dockerfile'
          dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
        stage('ubuntu1404') {
          agent { dockerfile { filename 'ubuntu1404.dockerfile'
          dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
        stage('ubuntu1604') {
          agent { dockerfile { filename 'ubuntu1604.dockerfile'
          dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
        stage('ubuntu1804') {
          agent { dockerfile { filename 'ubuntu1804.dockerfile'
          dir '.dockerfiles' } }
	        steps { sh 'cat /etc/os-release' }
        }
       }
    }
  }
}
