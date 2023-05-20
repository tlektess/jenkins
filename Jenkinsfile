pipeline {
    agent any
    
    parameters {
        string(name: 'name', defaultValue: 'first-pipeline', description: 'first-pipeline')
        choice(name: 'env_name', choices: ['dev', 'qa', 'prod'], description: 'Application Environments to deploy'
        booleanParam(name: 'create_ec2', defaultValue: false, description: 'whether or not to create ec2')       
               }

    stages {
        // stage('SCM Checkout'){
        //     steps{
        //         git branch: 'main', credentialsId: 'sshkey', url: 'git@github.com:seytech-devops/jenkins.git'
        //     }
        // }
        stage('Terraform Init') {
            steps {
                sh "echo 'deploying into ${env_name}'"
            }
        }
        stage('Terraform Plan'){
            steps {
                sh "echo 'terraform plan'"
            }
        }
        stage('Terraform Apply'){
            steps {
                sh "terraform apply"
            }
        }
    }
}
