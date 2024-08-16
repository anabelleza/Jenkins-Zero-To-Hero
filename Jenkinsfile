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
                      'ls' 
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
