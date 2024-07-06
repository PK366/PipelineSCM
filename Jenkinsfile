pipeline{
    tools{
        maven 'mymaven'
    }
    agent any
    stages{
        stage('Clone the code'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Parallel Jobs'){
            parallel{
                stage('Compile the code'){
                    steps{
                        sh 'mvn compile'
                    }
                }
                stage('Test the Code'){
                    steps{
                        sh 'mvn test'
                    }
                }
                stage('Code Review'){
                    steps{
                        sh 'mvn pmd:pmd'
                    }
                }
            }
        }
    }
}
