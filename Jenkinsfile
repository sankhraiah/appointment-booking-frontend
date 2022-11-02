pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "npm run  build"
                sh "nohup npm start &"
            }
        }
        stage("Deploy") {
            steps {
                sh "rm -rf /var/www/NodeJS-Pipeline-Job"
                sh "cp -r ${WORKSPACE} /var/www/NodeJS-Pipeline-Job/"
            }
        }
    }
}
