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

                python '''
                print ("hi")
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

        stage('Post actions') {

            post {
                always {
                    archiveArtifacts *.zip
                }
            }
        }
    }
}