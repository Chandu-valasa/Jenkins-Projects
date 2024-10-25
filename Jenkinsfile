/* groovylint-disable-next-line NglParseError */
pipeline {
    agent {label 'node01'}

    stages {
        stage(Checkout) {
            steps {
                git url:'https://github.com/Chandu-valasa/django-notes-app.git', branch:'main'
            }
        }
        stage(build) {
            steps {
                sh'docker build -t shekar:1 .'
            }
        }
        stage(pushimage) {
            steps {
                script {
                   sh 'dockercred("Docker","dockerpass","dockeruser","shekar","1")'
                }
            }
        }
    
}
