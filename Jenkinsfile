pipeline {
    agent any

    stages {
        stage('DOCKER') {
             steps {
                                  script{
                                         //sh 'cp -r ../shared-library@2/target .'
                                         sh 'docker build . -t varunchughtech/varun-testone:five'
                                           // withCredentials([gitUsernamePassword(credentialsId: 'Jenkins_Private-Key', gitToolName: 'Default')]) {
    // some block
// } 

                                              sh 'docker login -u varunchughtech -p Reetchugh@2015   '
                                              sh 'docker push varunchughtech/varun-testone:five'
                                          //}
                                  }
        }
    }
}
}
