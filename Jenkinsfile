pipeline {
    agent any
    environment {
        UNIT_CODE="SIT753 - Professional Practice in IT"
        UNIT_EXERCISE="Week6 Exercise: Jenkins with GitHub"
    }
    stages {
        stage('Build') {
            steps {
                echo "$UNIT_CODE"
                echo "Installing build tools such as Gradle."
                echo "SIT753 Unit Exercise: Finished Build stage"
            }
        }
        stage('Test') {
            steps {
                echo "SIT753 Unit Exercise: Unit tests"
                echo "Peforming unit test using tools such as Junit."
                echo "SIT753 Unit Exercise: Intergration tests"
                echo "Performing integration test using tools such as Jvnet."
                echo "SIT753 Unit Exercise: Finished Test stage"
            }
            post {
                always {
                    echo "$UNIT_EXERCISE"
                    echo "SIT753 Unit Exercise: Test stage"
                }
                success {
                    emailext (attachLog: true,
                              to: "s223749059unitexercises@gmail.com",
                              subject: "SIT753 UnitExercise Week6 - Jenkins with GitHub - Test stage",
                              body: "SIT753 Unit Exercise: Stages completed")
                }
                failure {
                    mail (to: "s223749059unitexercises@gmail.com",
                         subject: "SIT753 UnitExercise Week6 - Jenkins with GitHub - Test stage",
                         body: "SIT753 Unit Exercise: Review stages")
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo "SIT753 Unit Exercise: Code analysis tool"
                echo "Applying code analysis tools such as CheckStyle."
                echo "SIT753 Unit Exercise: Finished Code Analysis stage"
            }
        }
        stage('Security Scan') {
            steps {
                echo "SIT753 Unit Exercise: Scanning tool"
                echo "Applying security scanning with probely-security-plugin."
                echo "SIT753 Unit Exercise: Finished Security Scan stage"
            }
            post {
                always {
                    echo "$UNIT_EXERCISE"
                    echo "SIT753 Unit Exercise: Security Scan stage"
                }
                success {
                    mail (to: "s223749059unitexercises@gmail.com",
                         subject: "SIT753 UnitExercise Week6 - Jenkins with GitHub - Security Scan stage",
                         body: "SIT753 Unit Exercise: Stages completed")
                }
                failure {
                    mail (to: "s223749059unitexercises@gmail.com",
                         subject: "SIT753 UnitExercise Week6 - Jenkins with GitHub - Security Scan stage",
                         body: "SIT753 Unit Exercise: Stages completed")
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "SIT753 Unit Exercise: Staging environment"
                echo "The application is completed deployed to staging server such as AWS EMR."
                echo "SIT753 Unit Exercise: Finished Staging stage"
            }
        }
        stage('Test on Staging') {
            steps {
                echo "SIT753 Unit Exercise: Integration Tests"
                echo "Performing integration test using tools such as Jvnet."
                echo "SIT753 Unit Exercise: Finished Test on Staging stage"
            }
            post {
                always {
                    echo "$UNIT_EXERCISE"
                    echo "SIT753 Unit Exercise: Test on Staging stage"
                }
                success {
                    mail (to: "s223749059unitexercises@gmail.com",
                         subject: "SIT753 UnitExercise Week6 - Jenkins with GitHub - Test on Staging stage",
                         body: "SIT753 Unit Exercise: Stages completed")
                }
                failure {
                    mail (to: "s223749059unitexercises@gmail.com",
                         subject: "SIT753 UnitExercise Week6 - Jenkins with GitHub - Test on Staging stage",
                         body: "SIT753 Unit Exercise: Stages completed")
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "SIT753 Unit Exercise: Production environment"
                echo "The application is completed deployed to production server such as AWS EMR"
                echo "SIT753 Unit Exercise: Finished Deploy to Production stage"
            }
        }
    }
}
