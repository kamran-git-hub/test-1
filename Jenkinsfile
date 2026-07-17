pipeline {
    agent any
    
    // Tools block Jenkins ko batata hai ki 'Maven3' ko is pipeline mein available karo
    tools {
        maven 'Maven3' 
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Code clone ho raha hai...'
                // Yahan aap git 'url' wali command use kar sakte hain
            }
        }
        stage('Build with Maven') {
            steps {
                echo 'Maven ke zariye code build aur package ho raha hai...'
                // 'mvn package' maven ki command hai jo code ko compile karke jar/war banati hai
                sh 'mvn package' 
            }
        }
    }
}
