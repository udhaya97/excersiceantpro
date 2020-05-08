def antVersion = 'Ant_1.10.7'

def callAnt(String Parameters) {
    if (isUnix()) {
        env.PATH = "${tool 'ant'}/bin;${env.PATH}"
        sh "ant ${Parameters}"
    }
    else {
        env.PATH = "${tool 'ant'}\\bin;${env.PATH}"
        bat "ant ${Parameters}"
    }
}


pipeline {
    agent any 
    stages {
        stage('Build') {
            steps { callAnt("-v -p")

   
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
