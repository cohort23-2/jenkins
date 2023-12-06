// # Declarative Jenkins Pipeline 
pipeline {
    agent none  //Global agent
    
    // global environments
    environment {
        NAME="Kanat"
    }

    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: "", artifactNumToKeepStr: "", daysToKeepStr: "10", numToKeepStr: "8")
    }

    parameters {
        string(name: "BRANCH_NAME", defaultValue:"", description: "The Git Branch name to build from")
        choice choices: ["init", "plan", "apply", "destroy"], description: "The terraform options to apply to", name: "TFCHOICE"
    }

    // trigger {

    // }
    
    stages {
        stage("Initialization on Windows") {
            agent any
            steps {
                // 
                echo "Initializating on Windows"
                echo "Your name is ${NAME}"
            }
        }
        stage("Initialiation on Linux") {
            agent any
            steps {
                echo "Initializating on Linux "
            }
        }
        stage("Build"){
            steps{
                //
                echo "Building artifact"
            }
        }
        stage("Test"){
            steps{
                echo "Testing ..."
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying ..."
            }
        }
    }
}

