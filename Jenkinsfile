pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                withAnt(Ant :'Ant')
                {
                  sh 'ant build'
                 
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
