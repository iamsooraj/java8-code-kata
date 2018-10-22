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
            
            }
        }


        stage ('Deployment Stage') {
            steps {

                    sh 'mvn --settings settings.xml deploy'

            }
        }
    }
}
