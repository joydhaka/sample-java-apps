def label = "worker-${UUID.randomUUID().toString()}"
podTemplate(label: label, containers: [
  containerTemplate(name: 'maven', image: 'eu.gcr.io/jenkins-demo/dind-jdk8-maven3:v4', command: 'cat', ttyEnabled: true),
]) {
  node(label) {
    def myRepo = checkout scm
    def gitCommit = myRepo.GIT_COMMIT
    def gitBranch = myRepo.GIT_BRANCH
    def shortGitCommit = "${gitCommit[0..10]}"
    def previousGitCommit = sh(script: "git rev-parse ${gitCommit}~", returnStdout: true)    
      
      stages {  
        stage('set build name')   {
            steps {
                sh 'echo my name is joy' 
            }
        }
}
    
}
    
