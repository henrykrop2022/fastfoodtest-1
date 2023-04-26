pipeline {
    agent any
    tools{
        maven 'M2_HOME'
    }
    stages{
        stage ("SCM"){
            steps {
                git branch: 'main', url: 'https://github.com/henrykrop2022/fastfoodtest-1.git'

            }
        }
        stage("Build & SonarQube Analysis") {
            steps{
                script{
                    dir('./fastfood_backend/'){
                  withSonarQubeEnv(credentialsId: 'sonarqube-id') {
                    sh 'mvn clean verify sonar:sonar
                     -Dsonar.projectKey=fast-food-2 \
                     -Dsonar.login=fastfood1'
                       }
                    }
                }
            }
        }
    }
}