pipeline {
    agent any
environment {
		//PATH = "${PATH}:${getMavenPath()}"
		DOCKER_TAG = "${getLatestCommitId()}"
		//NEXUS_HOST = "172.31.45.145:8083"
	//	DEV_IP = "3.108.54.171"
	}
    stages {
        stage('DOCKER') {
             steps {
                                  script{
                                         //sh 'cp -r ../shared-library@2/target .'
                                         sh 'docker build . -t varunchughtech/varun-testone:${DOCKER_TAG}'
                                           // withCredentials([gitUsernamePassword(credentialsId: 'Jenkins_Private-Key', gitToolName: 'Default')]) {
    // some block
// } 

                                              sh 'docker login -u varunchughtech -p Reetchugh@2015   '
                                              sh 'docker push varunchughtech/varun-testone:${DOCKER_TAG}'
                                          //}
                                  }
        }
    }
}
}
//to get docker image tag as per git commit id
def getLatestCommitId(){
	def commitId = sh returnStdout: true, script: 'git rev-parse HEAD'
	//def commitId = sh script: 'git rev-parse HEAD'
	return commitId
}
