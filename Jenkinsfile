pipeline {
    agent any

    stages {
        stage('app1 Build') {
                when {
                    changeset "**/app1/*.*"
                }
                steps {
                    dir('app1') {
                        sh "app1 processed" > log.txt
                    }
                }
        }
        stage('app2 Build') {
                when {
                    changeset "**/app2/*.*"
                }
                steps {
                    dir('app2') {
                        sh "app2 processed" > log.txt
                    }
                }
        }
        stage('app3 Build') {
                when {
                    changeset "**/app3/*.*"
                }
                steps {
                    dir('app3') {
                        sh "app3 processed" > log.txt
                    }
                }
        }
    }
    
}
