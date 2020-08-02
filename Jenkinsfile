pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh 'cd java-web-project'
                sh 'mvn -DskipTests clean package'
            }
        }
        stage("Test"){
            steps{
                sh 'mvn test'
            }
        }
    }
}
