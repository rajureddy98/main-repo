def Git_checkout(branch) {
    echo 'branch = '+"${microservice}"
    git 'https://github.com/rajureddy98/'+branch
}

pipeline {
    agent any
 
    stages {
        stage('parent-build'){
            steps {
                sh 'mvn clean package'
            }
        }
        stage('scm checkout') {
            steps {
                sh 'mkdir '+"${microservice}"
                sh 'cd '+"${microservice}"
                Git_checkout("${microservice}")
            }
        }
        stage('ms-pob-build'){
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
