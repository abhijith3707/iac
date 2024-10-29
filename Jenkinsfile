pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the Git repository
                git url: 'https://github.com/abhijith3707/iac.git', branch: 'main'
            }
        }

        stage('Terraform init') {
            steps {
                // Initialize Terraform
                sh 'terraform init'
            }
        }

        stage('Terraform apply') {
            steps {
                // Apply Terraform configuration
                sh 'terraform apply -auto-approve'
            }
        }
    }
}

