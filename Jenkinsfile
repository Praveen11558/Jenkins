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
            
                    sh 'mvn clean install'
               
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
