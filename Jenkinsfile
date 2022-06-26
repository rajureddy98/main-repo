def Git_checkout(branch) {
    echo 'branch = '+"${microservice}"
    git 'https://github.com/rajureddy98/'+branch
}

pipeline {
    agent any
 
    stages {
        stage('Hello') {
            steps {
                sh 'mkdir '+"${microservice}"
                sh 'cd '+"${microservice}"
                Git_checkout("${microservice}")
            }
        }
        stage('maven'){
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
