pipeline {
agent any
stages {
//  stage('scm checkout')             //download the code, scm: source code management
//  {steps {sh 'git clone https://github.com/prakashk0301/maven-project/' } }       //if no branch defined then it will download the code from default branch"master"

  stage('scm checkout')
  {steps {git branch: 'master', url: 'https://github.com/prakashk0301/maven-project/' }}
 
  stage('execute unit test framework')
  {steps {withMaven(globalMavenSettingsConfig: '6ae3dfc3-6ab7-4e7b-a9bd-418f757884b0', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '90c73295-0087-412a-9860-16baf9cf34f2') 
{
    sh 'mvn test'
}}}
  
  
    stage('create deployable package')
  {steps {withMaven(globalMavenSettingsConfig: '6ae3dfc3-6ab7-4e7b-a9bd-418f757884b0', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '90c73295-0087-412a-9860-16baf9cf34f2') 
{
    sh 'mvn clean package'
}}}
  
}
}
