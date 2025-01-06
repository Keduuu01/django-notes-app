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
                script{
                    build()
                }
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
                script{
                    deploy()
                }
            }
        }
    }
}
