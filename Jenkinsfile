pipeline{
    agent{
        label "agent-1"
    }
    options{
        timeout(time: 10, unit: 'SECONDS')
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
                sh 'sleep 10'
            }
        }
        stage('Deploy'){
            steps{
                echo "this is a Deploy"
                //error 'pipeline failed'
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
