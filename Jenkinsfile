pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the application.'
                echo 'Tool: Maven.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Test individual components and check that components work together.'
                echo 'Tools: JUnit for unit tests and Maven Failsafe for integration tests.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse code quality, coding standards and maintainability.'
                echo 'Tool: SonarQube.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan project dependencies for known security vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to an AWS EC2 staging server.'
                echo 'Tool: AWS CodeDeploy.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run API integration tests in staging to verify application behaviour in a production-like environment.'
                echo 'Tool: Newman, the command-line runner for Postman collections.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the verified application to an AWS EC2 production server.'
                echo 'Tool: AWS CodeDeploy.'
            }
        }
    }
}
