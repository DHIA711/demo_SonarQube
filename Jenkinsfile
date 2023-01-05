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
                 sh 'mvn sonar:sonar -Dsonar.projectKey=demo_sonar  -Dsonar.host.url=http://sonarqube:9000 -Dsonar.login=-Dsonar.login=966690e954f8023d0d052776ee16afa1f1055d5e'
                       }
             }

   }

}
