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
                sh'docker build -t chandu .'
            }
        }
        stage(test) {
            steps {
                sh 'echo hello world'
            }
        }
    }
}
