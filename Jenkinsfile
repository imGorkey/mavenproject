pipeline
{
agent none
stages
{
 stage('scm checkout')
 { agent { label: 'JAVA' }
  steps { git branch: 'master', url: 'https://github.com/prakashk0301/mavenproject' }}

}
}
