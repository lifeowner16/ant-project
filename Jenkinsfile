pipeline {
    agent any

    stages {

        stage ('SCM Checkout') {          
            steps {
              git 'https://github.com/lifeowner16/ant-project'
                }
            }   
        
         stage ('Compile Stage') {
            steps {
                withAnt(compile: 'ant') {
                    sh 'ant compile'
                }
            }
        }
    } 
}    
