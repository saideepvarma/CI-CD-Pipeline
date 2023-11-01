node {
   def mvnHome
  stage('Prepare') {
      git url: 'https://github.com/Nandeesh5208/b810am.git', branch: 'main'
      mvnHome = tool 'maven'
   }
  stage ('Code Scanning') {
      sh "'${mvnHome}/bin/mvn' sonar:sonar"
  }
  stage ('Clean') {
      sh "'${mvnHome}/bin/mvn' clean"
  }
  stage ('Validate') {
      sh "'${mvnHome}/bin/mvn' validate"
  }
  stage ('Compile') {
      sh "'${mvnHome}/bin/mvn' compile"
  }
  stage ('Test') {
      sh "'${mvnHome}/bin/mvn' test"
  }
  stage ('Install') {
      sh "'${mvnHome}/bin/mvn' install"
  }
  stage ('Verify') {
      sh "'${mvnHome}/bin/mvn' verify"
  }
  stage ('Package') {
      sh "'${mvnHome}/bin/mvn' package"
  }
}
