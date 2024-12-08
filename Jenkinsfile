pipeline{
    agent{ label "Worker"}
    
    stages{
        stage("code clone"){
            steps{
                sh "git clone https://github.com/Divyansh-Gupta2702/node-todo-cicd.git"
            }
        }
        stage("docker build"){
            steps{
                sh "docker build -t node-app ."
            }
        }
        stage("deploy"){
            steps{
                sh "docker compose down && docker compose up -d --build"
            }
        }
        
    }
}
