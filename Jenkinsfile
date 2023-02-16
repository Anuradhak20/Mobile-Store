pipeline{
     agent any
      stages{
         stage ('checkout the code from SCM'){
            steps{
                 echo 'checkout the code'
                  }
            }
        }
<<<<<<< HEAD
    }
=======
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
                    -Dsonar.host.url=http://172.174.142.7:9000 \
                    -Dsonar.login=sqp_b2528b6d7e51fffabd919f84ed3dc0a243c558b9
                    '''
            }
        } 
    }
}
>>>>>>> 28bb895fef260e4a28c45768f3d1374d0c0fa17f
