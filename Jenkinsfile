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
                    buildApp.checkout()
                }
            }
        }
        stage("Build Application") {
            steps {
                script{
                    buildApp.build()
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