@Library("github-api-global-lib@main") _

pipeline {
    agent any
    
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
                    pegadaianDemo.tfVars()
                }
            }
        }
    }
}