pipeline { 
    agent any  
    stages { 
        stage('Test') {
            steps {
                sh 'mvn clean test'
            }
            post {
                always {
                    emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
                }
            }
        }
    }
}
