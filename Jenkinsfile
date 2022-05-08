#!/usr/bin/env groovy
pipeline {
    agent any

    tools {
        nodejs "NODE"
    }

    stages{
        stage('Checkout') {
            steps{
                 git changelog: false, poll: false, url: 'https://github.com/marcelorbp/music.git'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'node test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy somewhere!'
            }
        }
    }
}
