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
        stage('Terraform destroy'){
            steps{
            sh 'terraform destroy --auto-approve'
        }
        }
    }
}
