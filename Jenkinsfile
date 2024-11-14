pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage("Echo Maven Version"){
            steps{
                echo "M398 --version"
            }
        }
        stage("install python"){
            steps{
                sh "sudo apt update -y"
                sh "sudo apt upgrade -y"
                sh "sudo apt install python3 -y"
            }
        }
        stage("Run Python Script"){
            sh "cd /var/lib/jenkins/workspace/jenkins_learn_master/"
            sh "python hello.py"
        }
        stage("Unit Test"){
            script{
                for(int i=0;i<5;i++){
                    echo "${i+1}"
                    sleep 1
                }
                echo "Python Script Executed Successfully....!"
        }
        }
    }
}
