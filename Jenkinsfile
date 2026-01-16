pipeline {
    agent any

    environment {
        STAGING_ENVIRONMENT = 'SIT753-Staging-task1'
        PRODUCTION_ENVIRONMENT = 'SIT753-Production-task1'
    }

    stages {
        stage('Build') {
            steps {
                echo "Build: compile and package"
                echo "Tool: Maven"
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo "Tests: unit tests + integration tests"
                echo "Tool: Jest"
            }
        }

        stage('Code Analysis') {
            steps {
                echo "Code Analysis: check code quality"
                echo "Tool: SonarCloud"
            }
        }

        stage('Security Scan') {
            steps {
                echo "Security Scan: scan for vulnerabilities"
                echo "Tool: npm audit"
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deploy to Staging: ${STAGING_ENVIRONMENT}"
                echo "Tool: AWS EC2"
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo "Staging Integration Tests: run tests on staging"
                echo "Tool:  Cypress"
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploy to Production: ${PRODUCTION_ENVIRONMENT}"
                echo "Tool: AWS EC2"
            }
        }
    }
}
