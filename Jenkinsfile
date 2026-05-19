pipeline {
    agent any

    stages {
        stage('Disk usage') {
            steps {
                sh 'echo "=== Disk partitions usage ==="'
                sh 'df -h'
            }
        }

        stage('Memory top process') {
            steps {
                sh 'echo "=== Process using most memory ==="'
                sh 'ps aux --sort=-%mem | head -2'
            }
        }
    }

    post {
        always {
            sh 'echo "Monitoring finished"'
        }
    }
}
