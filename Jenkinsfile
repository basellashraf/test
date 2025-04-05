pipeline {
    agent any

    parameters {
        string(name: 'BranchName', defaultValue: 'main', description: 'Enter the branch name for the build.')
        choice(name: 'Environment', choices: ['dev', 'test', 'prod'], description: 'Choose the deployment environment.')
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: "${params.BranchName}", url: 'https://github.com/basellashraf/test.git'
                }
            }
        }

        stage('Build') {
            steps {
                echo "Building project for environment: ${params.Environment}"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to ${params.Environment} environment"
            }
        }
    }
}
