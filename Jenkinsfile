pipeline
{
agent any 
stages
{
 stage('scm checkout')
 { steps { git branch: 'master', url: 'https://github.com/prakashk0301/mavenproject' }}


 stage('code compile')
 {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true)  {
    sh 'mvn compile'
 } }}

  stage('execute unit test framework')
 {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true)  {
    sh 'mvn test'
 } }}

   stage('code build')
 {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true)  {
    sh 'mvn package'
 } }}

 stage('deploy to tomcat server')
  {steps { sshagent(['deploy-to-tomcat']) 
   {
    sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ec2-user@172.31.20.221:/usr/share/tomcat/webapps'

   } }}

}
}