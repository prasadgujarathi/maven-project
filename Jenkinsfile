pipeline {

agent any 

stages {

      //stage ('scm checkout')
      //{steps{ sh "git clone https://github.com/prasadgujarathi/maven-project/"} }  //if no branch defiend it will download code from and master
      stage ('scm checkout')
      {steps {git branch: 'master', url: 'https://github.com/prasadgujarathi/maven-project'}}
      stage ('execute Unit test framework')
      {steps {withMaven(globalMavenSettingsConfig: '5487d52a-3b5d-4cd0-969d-856c389b2a94', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: 'f4558d63-9968-4341-b7e2-86fe15b7393d') {
    sh 'mvn test'
}}}
}
}
