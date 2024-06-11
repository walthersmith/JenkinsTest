pipeline{
    agent any

    stages {
        stage('Build'){
            steps{
                script {
                    sh 'javac src/sample/Hello.java'
                    sh 'cd src ; jar cf Hello.jar sample/Hello.class'
                }
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'src/Hello.jar', finger
            }
        }
    }
}