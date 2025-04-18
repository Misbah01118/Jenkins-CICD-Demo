pipeline {
    agent any

    tools {
        maven 'Maven 3'  // 👈 This must exactly match the name in Global Tool Configuration
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo "✅ Build completed successfully!"
        }
        failure {
            echo "❌ Build failed!"
        }
    }
}
