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
    }
}