/* groovylint-disable-next-line NglParseError */
/* groovylint-disable-next-line CompileStatic */
@Library('my-shared-library') _
pipeline {
    agent {label 'node01'}

    stages {
        stage(Checkout) {
            steps {
                script{
                    git ('https://github.com/Chandu-valasa/django-notes-app.git', 'main')
                }
            }
        }
        stage(build) {
            steps {
                script {
                    dockerb('shekar', 'latest')
                }
            }
        }
        stage(pushimage) {
            steps {
                script {
                    dockercred('Docker', 'dockerpass', 'dockeruser', 'shekar', 'latest')
                }
            }
        }
    }
}
