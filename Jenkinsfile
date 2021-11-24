pipeline {
    agent any
    stages {
        stage('Print hello') {
            steps {
                echo 'Hello world!'
         sh '''#!/bin/bash
                 ps ax
         '''

            }
        }

        stage('Run Tests') {
            parallel {
                stage('Test On Windows') {
                    steps {
                        sh "sleep 1"
                    }
                }
                stage('Test On Linux') {
                    steps {
                        sh "df -h"
                    }
                    steps {
                        sh "ip a"
                    }
                }
            }
        }
    }
}
