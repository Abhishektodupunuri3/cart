@Library('roboshop-shared-library') _

 pipeline {
    agent any 
    stages {
        stage('Lint Checks') {
            steps {  
                script {
                    sample.info('CART')
                }
                sh "echo Installing JSlint"
                sh "npm i jslint"
                sh "node_modules/jslint/bin/jslint.js server.js || true"
            }
        }     
        stage('code compile') {
            steps {
                sh "npm install"
            }
        }                                         // end of stages
    }
}