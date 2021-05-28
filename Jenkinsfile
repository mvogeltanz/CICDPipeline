pipeline {
    //Directives
    agent any
    tools {

        maven 'maven'
    }

    stages {
        // Specify various stages and steps

        // stage 1: Build
        stage ('Build'){
            steps {
                sh 'mvn clean install package'
            }
        }

        // Stage 2: Test
        stage ('Test'){
            steps {
                echo 'testing...'

            }
        }

        //Stage 3: Deploy
        stage ('Deploy'){
            steps {
                echo 'deploying...'
            }
        }
    }
}