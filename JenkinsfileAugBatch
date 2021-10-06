node
{
def mavenHome = tool name: "maven3.8.2"
    
stage('CheckOutCode'){
git branch: 'development', credentialsId: '5d0cf3f9-48a6-4c55-9867-26e5b5ae8e5d', url: 'https://github.com/vsss-ec-apps-test/maven-web-application.git'
}
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
/*  
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn clean sonar:sonar"
}

stage('UploadArtifactIntoNexusRepo'){
sh "${mavenHome}/bin/mvn clean deploy"
}

stage('DeploytheAppintoTomcat')
{
sshagent(['03f13e30-c60d-41b2-806a-3a5388d6d971']) {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.108.250.150:/opt/apache-tomcat-9.0.53/webapps"
}
}
*/



}
