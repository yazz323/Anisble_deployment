pipeline {
  agent any
  
  stages {
    stage('Install Ansible') {
      steps{
        script{
          sh 'yum -y install ansible'
        }
      }
    }
  
    stage('Deploy Ansible') {
      steps{
        script{
          sh "ansible-playbook -i inventory/inventory deploy_httpd.yml"
        }  
      }

    }
  
  }
}
