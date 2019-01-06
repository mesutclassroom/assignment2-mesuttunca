pipeline { 
    agent any  
    stages { 
        stage('Test') {
            steps {
                sh 'sudo mvn clean test'
            }
            post {
                always {
                     junit 'target/surefire-reports/*.xml'
                 }
            }
        }
    }
}
