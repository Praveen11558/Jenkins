pipeline {
    agent any

    stages {

stage ('Compile Stage') {

            steps {
            
                    mvn clean install
               
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
