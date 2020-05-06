pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
               def antVersion = 'Ant1.10.7'
withEnv( ["ANT_HOME=${tool antVersion}"] ) {
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
