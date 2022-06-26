pipeline {
agent any
environment {
        env.BRANCH = "account-service"
    }
stages {
    stage('build') {
        agent any
        steps {
            script {
                showMavenVersion('mvn version')
            }
        }
    }
}

}

def showMavenVersion(String branch) {
        echo 'https://github.com/rajureddy98/'"${env.BRANCH}"
        echo "${env.BRANCH}"
}
