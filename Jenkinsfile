@Library("github-api-global-lib@main") _

pipeline {
    agent none
    
    stages {
        stage("Testing Pipeline") {
            agent { any }
            steps {
                script {
                    greetingHello.world("Deni")
                }
            }
        }
    }
}