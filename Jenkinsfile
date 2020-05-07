def antVersion = 'Ant_1.10.7'
pipeline {
    agent any 
    stages {
        stage('Build') {
            steps { withEnv( ["ANT_HOME=${tool antVersion}"] ) {
    bat 'ant.bat'
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
