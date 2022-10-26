pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                bat "npm install --legacy-peer-deps"
                bat "npm run build"
            }
        }
        stage("Deploy") {
            steps {
                echo "${WORKSPACE}"    
                bat "rm -rf /var/www/jenkins-react-app"
                bat "cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}