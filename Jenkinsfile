node(){
  stage('Cloning git'){
    checkout scm
  }
}
node('ubuntu-apps'){
  stage ('Build') {
    git url: 'https://github.com/denialhaq/cicd.git'
    withMaven {
      sh "mvn clean verify"
    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
  }
}
    
