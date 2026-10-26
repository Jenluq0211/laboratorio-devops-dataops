pipeline {

    agent any

    stages {

        stage('Verificar Python') {
            steps {
                bat '"C:\\Certus_clases\\Lab_DataOps\\.venv\\Scripts\\python.exe" --version'
            }
        }

        stage('Procesamiento Dataset') {
            steps {
                bat '"C:\\Certus_clases\\Lab_DataOps\\.venv\\Scripts\\python.exe" scripts\\procesamiento.py'
            }
        }

    }

    post {

        success {
            echo 'Pipeline ejecutado correctamente'
        }

        failure {
            echo 'Pipeline falló'
        }

    }

}