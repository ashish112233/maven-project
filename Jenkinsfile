pipeline{

    agent any

    stages   {
        stage('Build'){

            steps{
                sh 'maven clean package'
            }

            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts : '**/target/*.war'
                }
            }
        }
        stage('Deploy to Staging'){

            steps{
                    echo 'Deploy to Staging stage from file'
            }
        }
    }
}