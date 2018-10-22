pipeline {
    agent any
     tools { 
        maven 'default maven'  
    }
    stages {
        stage ('Compile Stage') {

            steps {

		    sh 'mvn --settings settings.xml install -Dmaven.test.skip=true'

            }
        }

        stage ('Testing Stage') {

            steps {
             sh 'mvn --settings settings.xml package -Dmaven.test.skip=true'
            }
        }


        stage ('Deployment Stage') {
            steps {

                    sh 'mvn --settings settings.xml deploy'

            }
        }
    }
}
