pipeline {
    agent any

    stages {
        // stage('SCM Checkout'){
        //     steps{
        //         git branch: 'main', credentialsId: 'sshkey', url: 'git@github.com:seytech-devops/jenkins.git'
        //     }
        // }
        stage('Terraform Init') {
            steps {
                sh "echo 'terraform init'"
            }
        }
        stage('Terraform Plan'){
            steps {
                sh "echo 'terraform plan'"
            }
        }
        stage('Terraform Apply'){
            steps {
                sh "echo 'terraform apply'"
            }
        }
    }
}