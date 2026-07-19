pipeline {
    agent any
    
    tools {
        maven 'Maven3' 
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Code clone ho raha hai...'
                git url: 'https://github.com/jglick/simple-maven-project-with-tests.git', branch: 'master'
            }
        }
        stage('Build with Maven') {
            steps {
                echo 'Code build ho raha hai...'
                sh 'mvn clean package' 
            }
        }
        stage('Deploy with Ansible') {
            steps {
                echo 'Ansible Playbook ke zariye live server par deploy ho raha hai...'
                // Ansible playbook ko run karne ki command
                sh 'ansible-playbook -i inventory deploy_playbook.yml' 
            }
        }
    }
}
