pipeline {
    agent any
    environment {
        UNIT_CODE="SIT753 - Professional Practice in IT"
        UNIT_EXERCISE="Week6 Exercise: Jenkins with GitHub"
    }
    tools {
        nodejs "node"
        gradle "gradle"
    }
    stages {
        stage('Build') {
            steps {
                echo "$UNIT_CODE"
                echo "Installing yarn"
                sh "npm config ls"
                sh "npm install -g yarn"
                sh "yarn install"
                sh "./gradlew -v"
                echo "SIT753 Unit Exercise: Finished Build stage"
            }
        }
        stage('Test') {
            steps {
                echo "SIT753 Unit Exercise: Unit tests"
                echo "SIT753 Unit Exercise: Intergration tests"
                echo "SIT753 Unit Exercise: Finished Test stage"
            }
        }
        stage('Code Analysis') {
            steps {
                echo "SIT753 Unit Exercise: Code analysis tool"
                echo "SIT753 Unit Exercise: Finished Code Analysis stage"
            }
        }
        stage('Security Scan') {
            steps {
                echo "SIT753 Unit Exercise: Scanning tool"
                echo "SIT753 Unit Exercise: Finished Security Scan stage"
            }
        }
        stage('Staging') {
            steps {
                echo "SIT753 Unit Exercise: Integration tests"
                echo "SIT753 Unit Exercise: Finished Staging stage"
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "SIT753 Unit Exercise: The application is completed deployed to production server"
                echo "SIT753 Unit Exercise: Finished Deploy to Production stage"
            }
        }
    }
    post {
        always {
            echo "$UNIT_EXERCISE"
        }
        success {
            echo "SIT753 Unit Exercise: Jenkins with GitHub"
            echo "SIT753 Unit Exercise: Stages completed"
        }
        failure {
            echo "SIT753 Unit Exercise: Review stages"
        }
    }
}
