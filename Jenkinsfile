pipeline {
    agent any

    stages {
        stage('clone'){
            steps {
                script {
                    echo "this is clone stage"
                    sh "gffjfjjfjf "
                }
            }
        }

        stage('build'){
            agent {
                docker {
                   image 'python:3.7-buster'
                }
            
            }
            steps {
                script {
                        sh " python --version"
                }
            }
        }

        stage('deploy'){
             agent {
                docker {
                   image 'python:3.9-buster'
                }
            
            }
            steps {
                script {
                        sh " python --version"
                }
            }
        }
    }
    
    post{
        always{
          cleanWs()
        }
        
        failure {
           echo "pipeline failed will be sending failure mail"
        }
    }
}
