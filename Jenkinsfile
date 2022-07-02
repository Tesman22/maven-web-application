node
 {
  def mvnHome = tool name: "Maven3.8.6"
  stage("CheckOutCodeGit")
  {
   git credentialsId: 'Github', url: 'https://github.com/Tesman22/maven-web-application.git'
  } 
 stage("Build")
 {
 sh "${mavenHome}/bin/mvn clean package"
 }
  /*
 stage("ExecuteSonarQubeReport")
 {
 sh "${mavenHome}/bin/mvn sonar:sonar"
 }
 
 stage("UploadArtifactsintoNexus")
 {
 sh "${mavenHome}/bin/mvn deploy"
 }
 
  stage("DeployAppTomcat")
 {
  sshagent(['423b5b58-c0a3-42aa-af6e-f0affe1bad0c']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war  ec2-user@15.206.91.239:/opt/apache-tomcat-9.0.34/webapps/" 
  }
 }
 
 stage('EmailNotification')
 {
 mail bcc: 'mylandmarktech@gmail.com', body: '''Build is over

 Thanks,
 Landmark Technologies,
 +14372152483.''', cc: 'mylandmarktech@gmail.com', from: '', replyTo: '', subject: 'Build is over!!', to: 'mylandmarktech@gmail.com'
 }
 */
 
 }
