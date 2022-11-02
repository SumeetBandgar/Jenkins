@Library("shared-library") _

pipeline {
    agent any
    stages {
        stage("Checkout Repo") {
            steps {
                script {
                    checkout.call()
                }
            }
        }
        stage("Shared Library") {
            steps {
                helloWorld(name : "Sumeet", place : "Pune")
            }
        }
    }
}