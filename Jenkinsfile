pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', changelog: false, credentialsId: 'azure', poll: false, url: 'https://chetantalwar0584@dev.azure.com/chetantalwar0584/DemoProject2/_git/DemoProject2'
            }
        }
        stage('app1 Build') {
            steps {
                when {
                    changeset "**/app1/*.*"
                }
                steps {
                    dir('app1') {
                        sh "app1 processed" > log.txt
                    }
                }
            }
        }
        stage('app2 Build') {
            steps {
                when {
                    changeset "**/app2/*.*"
                }
                steps {
                    dir('app2') {
                        sh "app2 processed" > log.txt
                    }
                }
            }
        }
        stage('app3 Build') {
            steps {
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
    
}
