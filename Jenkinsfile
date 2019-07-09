pipeline {
    agent any

    stages {

        stage ('SCM Checkout') {          
            steps {
              git 'https://github.com/lifeowner16/ant-project'
                }
            }

        stage ('Compile Stage') {
         { agent label 'compile' }
            steps {
                withAnt(ant : 'ant') {
                    sh 'ant compile clean'

                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withAnt(maven : 'maven') {
                    sh 'ant test'
                }
            }
        }

        stage ('Package Stage') {
            steps {
                withAnt(maven : 'maven') {
                    sh 'ant package'
                }
            }
        }

        stage ('verify Stage') {
            steps {
                withAnt(maven : 'maven') {
                    sh 'ant verify'
                }
            }
        }
    }
} 
