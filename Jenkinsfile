pipeline
{
    agent any
    
    stages
    {
        stage('git checkout1')
        {
            steps
            {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/ashisnishanka/maven-class.git']]])
                echo "my git clone is successfully down to my workspace"
            }
        }
        stage('build')
        {
            steps
            {
                sh 'mvn compile'
                echo "my git build is successfully "
            }
        }
        stage('test')
        {
            steps
            {
                sh 'mvn test'
                echo "my testing is successfully "
            }
        }
        stage('package')
        {
            steps
            {
                sh 'mvn package'
                echo "my jar/war is successfully created "
            }
        }
    }
}
