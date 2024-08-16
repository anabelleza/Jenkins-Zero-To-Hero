pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/anabelleza/Jenkins-Zero-To-Hero.git'
            }
        }
        stage('Clean Workspace') {
            steps {
                // Clean up the workspace to remove any previous build artifacts
                cleanWs()
            }
        }
        stage('Build') {
            steps {
                sh './build.sh'  // Or use any other build command
            }
        }

        stage('Test') {
            steps {
                sh './run-tests.sh'  // Run your tests
<<<<<<< HEAD
                ls 
=======
                      'ls' 
>>>>>>> b88ba26ad6275ad644ac8d4d2435e16fba1abc8e
            }
        }
        stage('Test2') {
            steps {
                sh '''
                ./run-tests.sh    
                ls -al
                '''   
                
            }
        }

        
    }

    
}
