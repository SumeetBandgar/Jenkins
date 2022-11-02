@Library("shared-library") _

pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }
    stages {
        stage("Checkout Repo") {
            steps {
                script{
                    checkout.call()
                }
            }
        }
        stage("Build Application") {
            steps {
                script{
                    buildApp.call()
                }
            }
            
            post {
                success {
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}