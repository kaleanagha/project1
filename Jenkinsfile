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
