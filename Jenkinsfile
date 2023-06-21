pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    
    stages{
        stage('build'){
            steps{
                echo 'this is build the app job'
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'this is the test the app job'
                sh 'npm test'
            }
        }
        stage('package'){
            steps{
                echo 'this is the package the app job'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'Hello there this my first pipeline has completed through code...'
        }
        
    }
    
}
