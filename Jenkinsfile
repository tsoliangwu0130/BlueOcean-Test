pipeline {
    agent any
    stages {
        stage('one') {
            steps {
                sh 'echo 4730 > myfile.txt'
                script {
                    var = readFile('myfile.txt')
                }
            }
        }
        stage('two') {
            steps {
                echo "${var}"
            }
        }
    }
}
