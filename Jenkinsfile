@Library("github-api-global-lib@main") _

pipeline {
    agent none
    
    stages {
        stage("Generate Properties") {
            steps {
                script {
                    properties([
                        parameters([
                            string(defaultValue: '', name: 'OS_VERSION', trim: true),
                            // string(defaultValue: '', name: 'APP', trim: true)
                        ])
                    ])
                    currentBuild.displayName = "Sandbox-shared-Lib"
                }
            }
        }

        stage("Sytem Operasi Test") {
            steps {
                script {
                    if "${OS_VERSION}" == greetingHello.os("Windows") {
                        echo "your OS windows"
                    } else {
                        echo "OS unknown"
                    }
                }
            }
        }
    }
}