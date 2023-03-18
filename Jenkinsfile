pipeline {
    agent any
    environment{
        PATH="/opt/apache-maven-3.9.0/bin:$PATH"
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
         stage('gitclone') {
            steps {
               git branch: 'main', url: 'https://github.com/SRahamath/pipeline-jenkins.git' 
            }
        }
        stage('maven-build') {
            steps {
               sh"mvn -v"
            }
    }
}
}
