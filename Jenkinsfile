pipeline {
    agent any

    stages {
        stage ('Path') {

            steps {
                
                    sh 'ls -lat'
                
            }
        }

stage ('Compile Stage') {

            steps {
                withMaven(maven) {
                    sh 'mvn clean install'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven) {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven) {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
