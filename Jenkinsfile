pipeline{
    agent any
    triggers { 
        pollSCM('* * * * *')
         }
    stages {
        stage ('vcs')
        {
            steps{
                git url: 'https://github.com/rajujaggu/saleor-dashboard.git',
                  branch: 'main'
            }
        }
        stage ('build'){
            steps{
                sh 'docker image build -t rajreddy999/saleor-dashboard:Dev .'
                sh 'docker image push rajreddy999/saleor-dashboard:Dev'
            }
        }
    }
}