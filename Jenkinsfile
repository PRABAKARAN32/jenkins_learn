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
                sh "sudo apt upadte -y"
                sh "sudo apt upgrade -y"
                sh "sudo apt install python3 -y"
            }
        }
        stage("Run Python Script"){
            sh "cd /var/lib/jenkins/workspace/jenkins_learn_master/"
            sh "python hello.py"
        }
        stage(){
            script{
                for(int i=0;i<5;i++){
                    echo "${i+1}"
                    sleep 1
                }
                echo "Python Script Executed Sucessfully....!"
        }
        
        // stage("run python script"){
        //     steps{
                
        //     }
        // }
        // stage('Build') {
        //     steps {
        //         // Get some code from a GitHub repository
        //         git 'https://github.com/jglick/simple-maven-project-with-tests.git'

        //         // Run Maven on a Unix agent.
        //         sh "mvn -Dmaven.test.failure.ignore=true clean package"

        //         // To run Maven on a Windows agent, use
        //         // bat "mvn -Dmaven.test.failure.ignore=true clean package"
        //     }

        //     post {
        //         // If Maven was able to run the tests, even if some of the test
        //         // failed, record the test results and archive the jar file.
        //         success {
        //             junit '**/target/surefire-reports/TEST-*.xml'
        //             archiveArtifacts 'target/*.jar'
        //         }
        //     }
        // }
    }
}
