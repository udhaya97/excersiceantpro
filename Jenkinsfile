def antVersion = 'Ant_1.10.7'
pipeline {
    agent any 
    stages {
        stage('Build') {
            steps { env.PATH = "${tool 'ant'}\\bin;${env.PATH}"
        bat "ant ${Parameters}"

   
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
