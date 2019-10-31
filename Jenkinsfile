pipeline {
    agent any

    stages {
        stage ('Step1:Compile Stage') {

            steps {
                withMaven(maven : 'Maven_3_6_2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Step2:Testing Stage') {

            steps {
                withMaven(maven : 'Maven_3_6_2') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Step3:Deployment Stage') {
            steps {
                withMaven(maven : 'Maven_3_6_2') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
