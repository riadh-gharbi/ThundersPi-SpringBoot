pipeline {
    agent any
    stages {
        stage("Clone Git Repo"){
            steps{
            git branch: main, url : "https://github.com/riadh-gharbi/eduhub-springboot"
            }
        }
        stage("Show Date"){
            steps{
            sh "date"
            }
        }
    }

}