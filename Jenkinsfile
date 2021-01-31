pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                timeout(time: 3, unit: 'MINUTES') {
                    retry(5) {
                        sh "chmod +x -R ./flakey-deploy.sh"
                        sh './flakey-deploy.sh'
                    }
                }
            }
        }
    }
}
