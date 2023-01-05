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
                 sh 'mvn sonar:sonar -Dsonar.projectKey=demo_sonar -Dsonar.projectName=demo_sonar -Dsonar.host.url=http://127.0.0.1:9000 -Dsonar.login=755a851524cdca670ed0fa93f437bb06e41dbc11'
                       }
             }

   }

}
