pipeline{
    
    agent any
    
    stages{
        stage('Clone the repo'){
            steps{
                
                echo 'clone the repo Jenkins_SCM_Webhook_Demo1.git'
                sh 'rm -fr Jenkins_SCM_Webhook_Demo1'
                sh 'git clone https://github.com/mvishwa27/Jenkins_SCM_Webhook_Demo1.git'
                //sh '~/Desktop/V/tools/jenkins/scripts/git_clone_1.sh'
            }
        }
                stage('Push repo to remote host'){
            
            steps{
                echo 'connect to remote host and pull down the latest version'
                git branch: 'main', credentialsId: 'mvishwa27', url: 'https://github.com/mvishwa27/Jenkins_SCM_Webhook_Demo1.git'
                sh 'git remote -v'
                sh 'git pull origin main'
            }
            
        }
        
        
                stage('Stage-3'){
            
            steps{
                echo 'Stage 3 here'
            }
            
        }
        
        
    }
    
}
