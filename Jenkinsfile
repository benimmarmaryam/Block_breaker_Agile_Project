pipeline {
  
  agent any
  
  stages {
  
    stage("build") {
    
      steps {
        echo 'build'
        sh 'make'
      }
    }
    
    stage("test") {
    
      steps {
        echo 'test'
        sh 'make check || true' 
        junit '**/target/*.xml'
      }
    }
    
    stage("deploy") {
    
      steps {
        echo 'deploy'
        sh 'make publish'
      }
    }
  }
}
