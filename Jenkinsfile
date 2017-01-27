#!groovy

@NonCPS
def printParams() {
  env.getEnvironment().each { name, value -> println "Name: $name -> Value $value" }
}
// printParams() // requires permissions

node {
    stage('Build') {
      echo "building..."
      scm

      sh "mkdir -p output"

      echo "  display environment"
      sh 'env > output/env.txt'
      sh 'cat output/env.txt'

      archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md'              
    }

    stage('Test') {
      echo "testing..."
    }

    stage('Deploy') {
      echo "deploying..."
    }
}
