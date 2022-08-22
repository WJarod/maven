pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                echo 'Building ...'
                node {
                    stage ('Build') {
                        git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
                        withMaven {
                        sh "mvn clean verify"
                        } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
                    }
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
