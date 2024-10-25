pipeline{
    agent {label 'node01'}

    stages {
        stage(Checkout) {
            steps {
                git url:'https://github.com/Chandu-valasa/django-notes-app.git', branch:'main'
            }
        }
        stage(build){
            steps {
                sh 'echo hello world'
            }           
        }
    }









}