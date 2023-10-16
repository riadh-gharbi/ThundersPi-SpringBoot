pipeline{
    stages {
      stage("Cloning the project...") {
        steps {
            git branch: 'main', url: 'https://github.com/riadh-gharbi/eduhub-springboot.git'
        }
      }

      stage("Compilation using Maven") {
        steps {
            sh "./mvnw clean install -DskipTests"
        }
      }

      stage("Tests and Deployment") {
        stage("Running unit tests") {
            steps {
                sh "./mvnw test -Punit"
            }
        }
        stage("Deployment") {
            steps {
                sh 'nohup ./mvnw spring-boot:run -Dserver.port=8001 &'
            }
        }
      }
    }
}