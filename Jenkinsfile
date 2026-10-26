pipeline {

    agent any

    stages {

        stage('Verificar Python') {

            steps {
                bat 'python --version'
            }

        }

        stage('Procesamiento Dataset') {

            steps {
                bat 'python scripts/procesamiento.py'
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