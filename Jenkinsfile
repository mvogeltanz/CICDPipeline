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

        // Stage : Publish the artifacts to Nexus
        stage ('Publish to Nexus'){
            steps {nexusArtifactUploader artifacts: [[artifactId: 'VinayDevOpsLab', classifier: '', file: 'target/VinayDevOpsLab-0.0.4-SNAPSHOT.war', type: 'war']], credentialsId: '0868a1a6-c092-402b-a0d5-96937120346e', groupId: 'com.vinaysdevopslab', nexusUrl: '172.20.10.60:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'MyDevOpsLab-SNAPSHOT', version: '0.0.4-SNAPSHOT'

            }
        }

        //Stage 4: Deploy
        stage ('Deploy'){
            steps {
                echo 'deploying...'
            }
        }
    }
}