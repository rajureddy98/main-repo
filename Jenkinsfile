def Git_checkout(branch) {
    echo 'https://github.com/rajureddy98/'+branch
    echo $microservice
}

pipeline {
    agent any
 
    stages {
        stage('Hello') {
            steps {
                Git_checkout('accout-service')
            }
        }
    }
}
