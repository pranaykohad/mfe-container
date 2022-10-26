pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                bat "npm install --legacy-peer-deps"
                bat "npm run build"
            }
        }
    }
}