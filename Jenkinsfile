pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                sh "cd java-web-project && mvn clean package"
            }
        }
        stage("deploy"){
            steps{
                deploy adapters: [tomcat7(credentialsId: '51e1dce7-731f-4ade-8a32-443f751ed25c', 
                path: '', url: 'http://ec2-3-17-159-176.us-east-2.compute.amazonaws.com:8080/')], 
                contextPath: 'javawebapp', war: ' **/java-web-project.war'
            }
        }
    }
}
