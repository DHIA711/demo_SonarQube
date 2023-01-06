pipeline {
          agent any
          tools{
            maven 'maven'
          }

          stages{

            stage('new .jar ') {

                steps {
                   sh 'mvn clean install -DskipTests'
                      }
            }
             stage('Sonarqube') { 

                 steps {  
                 sh 'mvn sonar:sonar -Dsonar.projectKey=demo_sonar  -Dsonar.host.url=http://sonarqube:9000 -Dsonar.login=c74be14c7a7a3cd4ad707fbf659754ac3b56f2f3'
                       }
             }

   }

}
