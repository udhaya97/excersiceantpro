pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
               
withAnt( [ANT_HOME='Ant1.10.7'] ) {
    sh '$ANT_HOME/bin/ant target1 target2'
}
                 
            }
        }
        stage('Test') { 
            steps {
                 sh 'make check'
                junit 'reports/**/*.xml'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'make publish'
            }
        }
    }
}
