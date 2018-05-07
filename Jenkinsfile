pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building on master..'
            }
        }
        stage('Test') {
            when { branch "master" }
            steps {
                echo 'Testing on master..'
            }
        }
        stage('Feature Test') {
            when { branch "feature/*" }
            steps {
                echo 'testing feature on ' + env.BRANCH_NAME
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying on master....'
            }
        }
    }
}
