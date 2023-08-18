pipeline {
    stages{
        stage('Init'){
            step{
                script{
                    git(url: 'https://github.com/tortasdev/tortasdev.git', credentialsId: 'Git', branch: 'main')
                    sh "npm i"
                    sh "rm -rf *"
                }
            }
        }
    }
}