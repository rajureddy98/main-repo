pipeline {
agent any
stages {
    stage('build') {
        agent any
        steps {
            script {
                env.BRANCH = "account-service"
                showMavenVersion('mvn version')
            }
        }
    }
}

}

def showMavenVersion(String branch) {
        echo 'https://github.com/rajureddy98/"${env.BRANCH}"'
}
