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
                sh "sudo rm -rf /var/www/NodeJS-Pipeline-Job"
                sh "sudo cp -r ${WORKSPACE} /var/www/NodeJS-Pipeline-Job/"
            }
        }
    }
}
