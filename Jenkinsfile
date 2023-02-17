pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'make'
                echo 'build stage successful'
                build job: 'PES1UG20CS093-1'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './hello_exe'
                echo 'test stage successful'
            }
        }
        stage ('Deploy')
        {
            steps
            {
                echo 'Deployment successful'
            }
        }
    }
    post
    {
        failure
        {
            echo 'Pipeline failed'
        }
    }
}
