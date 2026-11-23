pipeline {

    agent {
        label 'linux-agent'
    }

    stages {

        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }

        stage('Build Application') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Verify WAR File') {
            steps {
                sh 'ls -lh target/'
            }
        }

    }
}
