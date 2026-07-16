pipeline {
    agent any
    
    // Yeh environment block hai jahan hum simple variables aur secrets inject kar rahe hain
    environment {
        // 1. Simple Environment Variable
        APP_NAME = 'My_Super_App'
        
        // 2. Secret Credentials ko securely inject karna
        // 'my-api-token' wahi exact ID hai jo aapne Step 1 mein Jenkins UI mein banayi thi
        API_TOKEN = credentials('my_token')
    }

    stages {
        stage('Build') {
            steps {
                // Simple variable ko use karne ka tareeqa
                echo "Building application: ${APP_NAME}"
            }
        }
        stage('Test Secret') {
            steps {
                // Secret variable ko bash script (sh command) mein use karna
                // Jenkins automatically console output mein isko hide (****) kar dega taake koi dekh na sake!
                sh 'echo "My secure token is: $API_TOKEN"'
            }
        }
    }
}
