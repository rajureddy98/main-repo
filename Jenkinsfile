pipeline {
agent any
environment {
        BRANCH = 'account-service'
    }
stages {
    stage('build') {
        agent any
        steps {
            script {
                showMavenVersion("${BRANCH}")
            }
        }
    }
}

}

def showMavenVersion(BRANCH) {
        echo 'https://github.com/rajureddy98/'"${BRANCH}"
        echo "${BRANCH}"
}
