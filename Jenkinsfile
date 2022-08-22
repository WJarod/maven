pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                echo 'Building ...'
            } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe & FindBugs & SpotBugs reports...
        }
        stage('test') {
            steps {
                echo 'Testing ...'
            }
        }
        stage('deploy') {
            steps {
                echo 'Deployment ...'
                echo 'Deployment OK'
            }
        }
    }
}
