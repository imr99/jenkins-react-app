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
                sh " rm -rf /var/www/python"
                sh " cp -r ${WORKSPACE}/build/ /var/www/python/"
            }
        }
    }
     
}
