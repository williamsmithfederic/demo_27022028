pipeline {
    agent any

    environment {
        REPERTOIRE = "/"
    }

    stages {
        stage('build') {
            steps {
                echo 'Construction...'
            }
        }

        stage('test') {
            steps {
                echo 'test...'
            }
        }

        stage('lister repertoire') {
            steps {
                sh '''
                    echo "Contenu du répertoire : $REPERTOIRE"
                    ls -la $REPERTOIRE
                '''
                echo 'déploiement...'
            }
        }
    }

    post {
        success {
            echo "Pipeline exécuté avec succès"
        }
        failure {
            echo "Le pipeline a échoué"
        }
    }
}
