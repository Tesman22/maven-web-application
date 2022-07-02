node
 {
  def mavenHome = tool name: "Maven3.8.6"
  stage("CheckOutCodeGit")
  {
   git credentialsId: 'Github', url: 'https://github.com/Tesman22/maven-web-application.git'
  } 
 stage("Build")
 {
 sh "${mavenHome}/bin/mvn clean package"
 }
 stage("ExecuteSonarQubeReport")
 {
 sh "${mavenHome}/bin/mvn sonar:sonar"
 }
 /*
 stage("UploadArtifactsintoNexus")
 {
 sh "${mavenHome}/bin/mvn deploy"
 }
 */
  stage("DeployAppTomcat")
 {
  deploy adapters: [tomcat9(credentialsId: '1', path: '', url: 'http://35.87.118.105:8080/')], contextPath: null, war: 'target/*war' 
  }
 /*
 stage('EmailNotification')
 {
 mail bcc: 'mylandmarktech@gmail.com', body: '''Build is over

 Thanks,
 Landmark Technologies,
 +14372152483.''', cc: 'mylandmarktech@gmail.com', from: '', replyTo: '', subject: 'Build is over!!', to: 'mylandmarktech@gmail.com'
 }
 */
 
 }
