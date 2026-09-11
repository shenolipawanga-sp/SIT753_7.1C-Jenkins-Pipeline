pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the source code and packaging it into a deployable artefact.'
                echo 'Tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests on individual components, then integration tests across the service and database layers.'
                echo 'Tools: JUnit for unit tests, REST Assured for API integration tests'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analysing the codebase for maintainability issues, duplication and coding standard violations.'
                echo 'Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Scanning the source and its third-party dependencies for known vulnerabilities and reporting any CVEs found.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the packaged artefact to the staging server for pre-production verification.'
                echo 'Tool: AWS EC2 with Ansible'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Re-running the integration suite against staging to confirm the application behaves correctly in a production-like environment.'
                echo 'Tools: Postman with Newman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Promoting the validated build to the production environment.'
                echo 'Tool: AWS EC2 with AWS CodeDeploy'
            }
        }
    }
}
