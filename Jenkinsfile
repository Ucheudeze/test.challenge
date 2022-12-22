pipeline{
    agent any 
    tools {
        terraform 'terraform'
    }
    stages {
        stage('Git Checkout'){
            steps{
            git branch: 'main', credentialsId: 'ucheudeze', url: 'https://github.com/Ucheudeze/test.challenge.git'
        }
    }
        stage('Terraform init'){
            steps{
            sh 'terraform init'
        }
        }
        stage('Terraform plan'){
            steps{
            sh 'terraform plan -destroy'
        }
        }
        stage('Terraform destroy'){
            steps{
            sh 'terraform destroy --auto-approve'
        }
        }
    }
}
