@Library('Shared')_

pipeline{
    agent {label "binod"}
    
    stages{
        stage("Code"){
            steps{
                script{
                    clone("https://github.com/AdityaGaikwad6430/django-notes-app.git","main")
                }
            }
        }
        stage("Build"){
            steps{
                echo "This is Building the code"
                sh "sudo docker build -t notes-app:latest ."
            }
        }
        stage("Test"){
            steps{
                echo "This is Testing the code "
                echo "Testing of code completed"
            }
        }
        stage("Deploy"){
            steps{
                echo "This is Deployment"
                sh "sudo docker compose up -d"
            }
        }
    }
}
