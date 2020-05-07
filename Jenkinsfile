pipeline {
    agent any 
    
    tools {
        ant 'Ant' 
    }
    stages {
        stage('Build') {
            steps { withEnv(ANT : 'Ant'){
                sh 'ant'
            }
            
        }
    }
    
        stage('Test') { 
            steps {
                 sh 'make check'
                junit 'src/com/employee/test/**/*Test*.java'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'make publish'
            }
        }
    }
}
