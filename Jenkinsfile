pipeline { 
    agent any  
  tools {
    maven 'M3'
  }
    stages { 
        stage('Test') {
            steps {
                sh 'mvn clean test'
            }
        }
    }
}
