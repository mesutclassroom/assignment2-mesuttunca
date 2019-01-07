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
                    emailext body: '${FILE,path="target/surefire-reports/tests.AssignmentTest.txt"}', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Your assignment submission results'
                }
            }
        }
    }
}
