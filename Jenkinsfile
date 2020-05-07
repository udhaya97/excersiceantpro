pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
               
withEnv( ANT_HOME='Ant' ) {
    sh 'ant'
}
                 
            }
        }
        stage('Test') { 
            steps {
                 sh 'make check'
                junit 'src/com/employee/test/**/*.java'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'make publish'
            }
        }
    }
}
