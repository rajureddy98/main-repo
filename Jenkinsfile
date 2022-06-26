def Git_checkout(branch) {
    echo 'branch'+"${microservice}"
    echo 'https://github.com/rajureddy98/'+branch
}

pipeline {
    agent any
 
    stages {
        stage('Hello') {
            steps {
                Git_checkout("${microservice}")
            }
        }
    }
}
