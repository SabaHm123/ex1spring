pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Récupère le code source depuis le dépôt Git
                checkout scm
            }
        }

        stage('Hello') {
            steps {
                echo 'Hello, Jenkins!'
            }
        }

        stage('Dev') {
            steps {
                // Commandes ou scripts pour l'environnement de développement
                echo 'Déploiement dans l\'environnement de développement'
                // Exemples :
                // sh 'npm install'
                // sh './run-dev.sh'
            }
        }

        stage('Test') {
            steps {
                // Exécution des tests
                echo 'Exécution des tests'
                // Exemples :
                // sh 'npm test'
                // sh './run-tests.sh'
            }
        }

        stage('Deploy') {
            steps {
                // Déploiement en production ou en staging
                echo 'Déploiement en production'
                // Exemples :
                // sh './deploy.sh'
            }
        }
    }

    post {
        success {
            echo 'Pipeline exécuté avec succès!'
        }
        failure {
            echo 'Échec du pipeline.'
        }
    }
}
