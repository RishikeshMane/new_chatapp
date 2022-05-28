pipeline {
agent any
 stages {
  stage('Build') {
   steps {
    sh 'rsync -av -e "ssh -o StrictHostKeyChecking=no -i /var/lib/jenkins/frontendone-new.pem" /var/lib/jenkins/workspace/Mak-01/  ubuntu@10.0.3.48:/home/ubuntu/new_chatapp'
   }
 }
 stage('Deploy') {
  steps {
   sh 'ssh -i /var/lib/jenkins/frontendone-new.pem ubuntu@10.0.3.48 sudo systemctl restart gunicorn'
  }
 }
}
}
