@Library("shared-library") _

pipeline {
    agent any
    stages {
        stage("Checkout Repo") {
            steps {
                checkout()
            }
        }
        stage("Shared Library") {
            steps {
                helloWorld(name : "Sumeet", place : "Pune")
            }
        }
    }
}