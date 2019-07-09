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
                withAnt(installation: 'LocalAnt') {
                    sh "ant compile"
                    }
                }
          }      
         stage ('Test Stage') {
            steps {
                withAnt(installation: 'LocalAnt') {
                    sh "ant test"
                    }
                }
          }      
         stage ('Build Stage') {
            steps {
                withAnt(installation: 'LocalAnt') {
                    sh "ant build"
                    }
               }           
          }    
     }
}
