node ('master') {
     checkout scm
         stage('Build') {
              withMaven(maven: 'localMaven') {
              bat 'mvn -Dmaven.test.failure.ignore clean package'
                                             }
                       }
         stage('Results') {
              junit '**/target/surefire-reports/TEST-*.xml'
              archive 'target/*.jar'
                           }
}
