pipeline{
    agent any
    options{
        timestamps()
        }
    stages{
        stage('checkout'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/krishnaduttPanchagnula/Jenkins_test']]])
            }
        }
        stage ("Build") {
            steps{
            sh 'python3 calc.py'
            }
        }
        stage ("TEST"){
            steps{
            sh 'pytest test_calc.py'
            
            }
        }
        
    }
}
