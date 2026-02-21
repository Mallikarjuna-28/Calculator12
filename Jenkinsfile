pipeline{
  agent any
  stages{
    stage('clone'){
      steps{
        git branch:'main',url:
          }
    }
    stage('compile'){
      steps{
        sh'javac Calculator.java'
      }
    }
    stage('build'){
      steps{
        sh'java Calculator 25 5'
      }
    }
  }
}
