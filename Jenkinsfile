pipeline {
    agent any

    stages {
        stage('Clone code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/laxmi916/my-site-aws.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp -r * /var/www/html/
                sudo systemctl restart apache2
                '''
            }
        }
    }
}
