/* groovylint-disable-next-line NglParseError */
/* groovylint-disable-next-line CompileStatic */
@Library('my-shared-library') _
pipeline {
    agent {label 'node01'}

    stages {
        stage('Checkout') {
            steps {  
                gitclone("https://github.com/Chandu-valasa/django-notes-app.git", "main")
            }
        }
        stage('build') {
            steps {
                script {
                    dockerb("chandu2305", "sample1", "latest")
                }
            }
        }
        stage('pushimage') {
            steps {
                script {
                    dockercred("chandu2305","sample1","latest")
                }
            }
        }
    }
}
