pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo yum install httpd -y'
                sh 'sudo systemctl start httpd'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo rm -rvf /var/www/html/*'
                sh 'sudo cp -r /var/lib/jenkins/workspace/Ecomm/* /var/www/html/'
            }
        }
    }
}
