pipeline { 
    agent any  
  tools {
    maven 'Maven 3.5.0'
  }
    stages { 
        stage('Test') {
            steps {
                sh 'mvn clean test'
            }
            post {
                always {
                     junit 'target/surefire-reports/*.xml'
                 }
            }
        }
    }
}
