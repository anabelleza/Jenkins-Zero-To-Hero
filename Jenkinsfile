pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/anabelleza/Jenkins-Zero-To-Hero.git'
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
                ls 
            }
        }

        stage('Deploy') {
            steps {
                sshagent(['your-ssh-credentials-id']) {
                    sh '''
                    scp -r * user@your-server:/path/to/deploy
                    ssh user@your-server 'cd /path/to/deploy && ./deploy.sh'
                    '''
                }
            }
        }
    }

    
i}
