pipeline {

    agent any

    stages {

        stage('Echoing') {

            steps {

                //
                sh '''
                echo "hi there"
                echo "groovy baby"
                echo "inside shell block"
                '''
            }

        }

        stage('Run Script') {

            steps {

                //
                sh '''
                sh ./run.sh
                '''

            }

        }

    }

    post {

        always {
            archiveArtifacts '*.zip'
        }
        
    }

}