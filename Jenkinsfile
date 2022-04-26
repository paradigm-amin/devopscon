pipeline {
    agent any

    tools {
        maven "MVN"
    }
    stages {
        stage('Build') {
            steps {
                println 'Cloning repository...'
                println 'XXX-XXX-XXX'
                git 'https://github.com/paradigm-amin/devopscon.git'
                println 'Starting the build...'
		sh "mvn clean install -Pci"
            }
            post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                }
            }
        }
    }
}
