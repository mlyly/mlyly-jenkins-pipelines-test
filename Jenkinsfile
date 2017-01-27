#!groovy

@NonCPS
def printParams() {
  env.getEnvironment().each { name, value -> println "Name: $name -> Value $value" }
}
// printParams() // requires permissions

node {
    stage('Build') {
      echo "building..."

      echo "  display environment"
      sh 'env > env.txt'
      sh 'cat env.txt'
}

    stage('Test') {
      echo "testing..."
    }

    stage('Deploy') {
      echo "deploying..."
    }
}
