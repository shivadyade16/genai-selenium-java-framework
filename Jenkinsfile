pipeline {
  agent any
  stages {
    stage('Checkout') { steps { checkout scm } }
    stage('Build') { steps { sh 'mvn -B -DskipTests clean package' } }
    stage('Start Grid') { steps { sh 'docker-compose -f docker-compose.yml up -d selenium' } }
    stage('Test') { steps { sh 'mvn -B test' } }
  }
  post {
    always {
      archiveArtifacts artifacts: 'logs/**, target/allure-results/**', fingerprint: true
      sh 'docker-compose -f docker-compose.yml down'
    }
  }
}
