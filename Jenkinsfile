pipeline
{
    agent any
    stages
    {
        stage('git checkout')
        {
            
            steps
            {
                
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/ashisnishanka/maven-class.git']]])
                
                
            }
        }
        
        stage('build')
        {
            steps
            {
                sh 'mvn compile'
            }
        }
        stage('testing')
        {
            steps
            {
                sh 'mvn test'
               // bat 'mvn test'
            }
        }
         stage('package')
        {
            steps
            {
                sh 'mvn package'
               // bat 'mvn test'
            }
        }
    }
    
    
    
}
