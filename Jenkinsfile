pipeline {
    agent {
        docker {
            image 'my_local_maven:3.8.6-openjdk-18' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}