pipeline {
    agent any
    environment {
        UNIT_CODE="SIT753 - Professional Practice in IT"
        UNIT_EXERCISE="Week5 Exercise: Jenkins with pipeline"
        DIRECTORY_PATH="/Users/s223749059@deakin.edu.au/path_to_the_directory/sit753unit_exercise/Jenkinsfile"
        TESTING_ENVIRONMENT="SIT753 Unit Exercise on Week5 - UAT Testing Environment"
        PRODUCTION_ENVIRONMENT="SIT753 Unit Exercise on Week5 - PROD Production Environment"
    }
    stages {
        stage('Build') {
            steps {
                echo "$UNIT_CODE"
                echo "SIT753 Unit Exercise: Fetch the source code from: $DIRECTORY_PATH"
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
        stage('Code Quality Check') {
            steps {
                echo "SIT753 Unit Exercise: Check the quality of the code"
                echo "SIT753 Unit Exercise: Finished Code Quality Check stage"
            }
        }
        stage('Deploy') {
            steps {
                echo "SIT753 Unit Exercise: Deploy the application to $TESTING_ENVIRONMENT"
                echo "SIT753 Unit Exercise: Finished Deploy stage"
            }
        }
        stage('Approval') {
            steps {
                echo "SIT753 Unit Exercise: Perform sleep command for ten seconds"
                sleep 10
                echo "SIT753 Unit Exercise: Finished Approval stage"
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "SIT753 Unit Exercise: The application is completed deployed to $PRODUCTION_ENVIRONMENT"
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
