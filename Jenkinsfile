pipeline{
    agent{
        label 'docker'
    }

    stages{

        stage('Build docker image  '){
            steps{
                script{
                    sh 'docker build -t my-image:latest -f Dockerfile.dev .'
                }
            }
        
                
        }
    
        stage('Test'){
        steps{
            script{
                env.DOCKER_BUILD = 1
                sh 'docker run my-image:latest npm test'
            }
        }
      }
    }
    
    
}