def antVersion = 'Ant_1.10.7'
pipeline {
    agent any 
    stages {
        stage('Build') {
            steps { withEnv( ["ANT_HOME=${tool antVersion}"] ) {
    sh 'ant build'
}
            
        }
    }
    
        stage('Test') { 
            steps {
                echo '${ant}'
                junit 'src/com/employee/test/**/*Test*.java'
            }
        }
        stage('Deploy') { 
            steps {
                echo '${ant}'
            }
        }
    }
}
