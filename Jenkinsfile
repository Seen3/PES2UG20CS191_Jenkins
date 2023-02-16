pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'make -C main'
        echo 'Build stage successful'
      }
    }
    stage('Test'){
      steps{
        sh './main/hello_exec'
        echo 'Test Stage Successful'
        post{
          always{
            junit 'target/surefire-reports/*.xml'
          }
        }
      }
    }
    stage('Deploy'){
      steps{
        sh ''
        echo 'Deployment Successful'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
