pipeline{
    agent{
        label "agent-1"
    }
    stages{
        stage('build'){
            steps{
                echo "this is a build"
            }
        }
        stage('Test'){
            steps{
                echo "this is a Test"
            }
        }
        stage('Deploy'){
            steps{
                echo "this is a Deploy"
                failure
            }
        }
    }
    post{
        always{
            echo "This section runs alway"
            deleteDir()
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section runs when pipeline failures"
        }
    }
}
