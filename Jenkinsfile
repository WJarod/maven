pipeline {
    agent any

    stages 
    {
        stage('Maven-Install')
        {
            steps 
            {
                withMaven(maven: 'maven3')
                {
                    sh 'mvn clean install'
                }
            }
        }
    }

}
