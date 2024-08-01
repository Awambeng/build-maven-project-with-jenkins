pipeline{
    agent any
    stages{
        stage('Clone repo and clean'){
            steps{
                sh "rm -rf build-maven-project-with-jenkins"
                sh "git clone https://github.com/Awambeng/build-maven-project-with-jenkins.git"
                sh "mvn clean -f build-maven-project-with-jenkins"
            }
        }
        stage('Test'){
            steps{
                sh "mvn test -f build-maven-project-with-jenkins"
            }
        }
        stage('Deploy'){
            steps{
                sh "mvn package -f build-maven-project-with-jenkins"
            }
        }
    }
}
