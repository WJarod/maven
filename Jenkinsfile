pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                echo 'Building ...'
                git 'https://github.com/apache/maven-sources/'
                withMaven {
                    sh 'mvn clean install'
                }
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
