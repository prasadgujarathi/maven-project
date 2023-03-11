pipeline {

agent any 

stages {

      stage ('scm checkout')
      {steps{ sh "git clone https://github.com/prasadgujarathi/maven-project/"} }  //if no branch defiend it will download code from and master

      stage ('execute Unit test framework')
      {steps {withMaven(globalMavenSettingsConfig: '--- Use system default settings or file path ---', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '--- Use system default settings or file path ---') {sh 'mvn test'}}}
}
}

