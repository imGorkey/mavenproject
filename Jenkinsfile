pipeline
{
agent none
stages
{
 stage('scm checkout')
 { agent { label: 'JAVA' }
  steps { git branch: 'master', url: 'https://github.com/prakashk0301/mavenproject' }}

 /*stage('code compile')
 { agent { label 'JAVA' }
steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true)  {
	sh 'mvn compile'
 } }}

  stage('execute unit test framework')
 {agent { label 'JAVA' }
   steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true)  {
	sh 'mvn test'
 } }}

   stage('code build')
 {agent { label 'JAVA' }
   steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true)  {
	sh 'mvn clean -B -DskipTests package'
 } }}


 stage('build docker image')
 {steps { sh 'docker build -t pkw0301/devops:tomcat .' }}*/

}
}
