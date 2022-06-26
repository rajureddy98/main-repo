def Greet(name) {
    echo "Hello ${name}"
}

pipeline {
    agent any
 
    stages {
        stage('Hello') {
            steps {
                Greet('NaiveSkill')
            }
        }
    }
}
