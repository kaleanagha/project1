pipeline {
  agent {
     label {
        label 'project1'
}
}
     stages {
        stage ('Install appache') {
            steps {
                sh 'yum install httpd -y'
}
}


 stage ('depoly index file') {
   steps {
  chmod -R 777 /mnt
  chmod 400 ohiokey2.pem      
  scp -i "ohiokey2.pem" index.file ec2-user@3.17.141.189:/mnt/project1/index.html /var/www/html/
}
}

  stage ('Service Stop') {
     steps {
             sh 'service httpd stop'
}
}

  stage ('Service Start') {
     steps {
             sh 'service httpd start'
}
}
}
}
