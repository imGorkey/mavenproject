pipeline
{
agent none
stages
{
 stage('scm checkout')
 { steps { git branch: 'master', url: 'https://github.com/prakashk0301/mavenproject' }}

 stage('code compile')
 {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MVN_HOME', mavenSettingsConfig: '', traceability: true)  {
	sh 'mvn compile'
 } }}


}
}
