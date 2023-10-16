pipeline {
    agent any
    stages {
        stage("Clone Git Repo"){
            steps{
            git url : "https://github.com/riadh-gharbi/eduhub-springboot.git"
            }
        }
        stage("Show Date"){
            steps{
            sh "date"
            }
        }
    }

}