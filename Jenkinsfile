pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "npm install -y"
                sh "CI=false npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/python"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/python/"
            }
        }
    }
     
}
