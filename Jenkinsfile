pipeline {

    agent any

    stages {

        stage('Verificar Python') {
            steps {
                bat 'py --version'
            }
        }

        stage('Procesamiento Dataset') {
            steps {
                bat 'py scripts/procesamiento.py'
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