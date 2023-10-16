pipeline{

    agent any
    stages {
      stage("Cloning the project...") {
        git branch: 'main', url: 'https://github.com/riadh-gharbi/eduhub-springboot.git'
      }

      stage("Compilation using Maven") {
        steps{
            sh "./mvnw clean install -DskipTests"
        }
      }

      stage("Tests and Deployment") {
        stage("Running unit tests") {
          sh "./mvnw test -Punit"
        }
        stage("Deployment") {
          sh 'nohup ./mvnw spring-boot:run -Dserver.port=8001 &'
        }
      }
    }
}