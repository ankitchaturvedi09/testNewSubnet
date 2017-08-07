pipeline {
  agent any
  stages {
    stage('Create New Subnet') {
      steps {
        echo 'Creating Pipeline'
        sh '''(cd /var/lib/jenkins/terraformPractice/; sudo git pull)
cp -f /var/lib/jenkins/variables/variables.tf variables.tf
cp -f /var/lib/jenkins/terraformPractice/newSubnet.tf newSubnet.tf
terraform init
terraform plan
terraform apply'''
      }
    }
  }
}