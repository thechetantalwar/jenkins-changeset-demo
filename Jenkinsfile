pipeline {
    agent any

    stages {
        stage('app1 Build') {
                when {
                    changeset "**/app1/*.*"
                }
                steps {
                    dir('app1') {
                        sh 'echo app1 > log.txt'
                    }
                }
        }
        stage('app2 Build') {
                when {
                    changeset "**/app2/*.*"
                }
                steps {
                    dir('app2') {
                        sh 'echo app2 > log.txt'
                    }
                }
        }
        stage('app3 Build') {
                when {
                    changeset "**/app3/*.*"
                }
                steps {
                    dir('app3') {
                        sh 'echo app3 > log.txt'
                    }
                }
        }
    }
    
}
