def Git_checkout(branch) {
    echo 'branch = '+"${microservice}"
    git 'https://github.com/rajureddy98/'+branch
}

pipeline {
    agent any
 
    stages {
        stage('scm checkout') {
            steps {
                sh 'mvn help:evaluate -Dexpression=settings.localRepository'
                sh 'mkdir '+"${microservice}"
                sh 'cd '+"${microservice}"
                Git_checkout("${microservice}")
            }
        }
        stage('parent-build'){
            steps {
                sh 'cd ..'
                sh 'pwd'
                sh 'mvn help:evaluate -Dexpression=settings.localRepository'
                sh 'mvn package'
            }
        }
        stage('ms-pob-build'){
            steps {
                sh 'cd '+"${microservice}"
                sh 'mvn clean package'
            }
        }
    }
}
