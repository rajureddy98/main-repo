def Git_checkout(branch) {
    echo 'branch = '+"${microservice}"
    git 'https://github.com/rajureddy98/'+branch
}

pipeline {
    agent any
 
    stages {
        stage('clean WS') {
            steps {
                cleanWs()
            }
        }
        stage('scm checkout') {
            steps {
                Git_checkout("${microservice}")
            }
        }
        stage('parent-build'){
            steps {
                sh 'mvn package'
            }
        }
    }
}
