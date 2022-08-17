pipeline {
    agent node2
    stages { 
        stage ('Stage1-Compile Stage') {
          
           steps { 
              withMaven(maven : 'Maven') {
                 sh 'mvn clean compile'
            }
        }
      }
      stage ('Testing Stage') {
           steps { 
              withMaven(maven : 'Maven') {
                 sh 'mvn test'
            }
        }
      }
            stage ('Deploy Stage') {
           steps { 
              withMaven(maven : 'Maven') {
                 sh 'mvn package'
            }
        }
      }

   }
}
