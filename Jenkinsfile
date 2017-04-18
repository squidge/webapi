#!/usr/bin/env groovy

node('master') {
    try {
        stage('build') {
            // Checkout the app at the given commit sha from the webhook
            checkout scm

            sh "dotnet restore"
            sh "dotnet build"
        }

        stage('test') {
            sh "echo 'WE ARE RUNNING SOME TEST'"
        }

        stage('deploy') {
            sh "echo 'WE ARE DEPLOYING'"
        }
    } catch(error) {
        throw error
    } finally {
        // Any cleanup operations needed, whether we hit an error or not
    }
}
