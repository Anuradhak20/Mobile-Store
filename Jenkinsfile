pipeline{
     agent any
      stages{
         stage ('checkout the code from SCM'){
            steps{
                 echo 'checkout the code'
                  }
            }
            stage ('Build the project'){
            steps{
                echo 'building the project'
                sh 'mvn clean install -DskipTests'
            }
         }
stage('Sonarqube'){
     steps{
         echo 'Sonar Codequality'
         sh '''
         mvn clean verify sonar:sonar \
          -Dsonar.projectKey=Mobilestore \
          -Dsonar.host.url=http://20.197.224.111:9000 \
          -Dsonar.login=sqp_3ed4962cdd00038a4f14ee3a57f3587008d9149a
         '''
          }
           }

        }
    }
