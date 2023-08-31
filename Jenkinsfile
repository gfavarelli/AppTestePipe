pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from the repository
                // This step will depend on your version control system
            }
        }
        
        stage('Run Tests') {
            steps {
                script {
                    if (env.RUN_TESTS == 'true') {
			echo 'RUNNING TESTS'
                        sh './gradlew clean test --tests "*.*.*SearchTest"'
                    } else {
                        echo 'No search-related changes detected. Skipping search tests.'
                    }
                }
            }
        }
        
        // Other stages...
    }
}