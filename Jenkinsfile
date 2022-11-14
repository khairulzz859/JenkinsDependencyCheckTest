pipeline {
  agent any
  stages {
    stage('OWASP DependencyCheck') {
      steps {
        dependencyCheck additionalArguments: '--format HTML --format XML --scan . --enableExperimental', odcInstallation: 'OWASP-Dependency-Check'
        dependencyCheckPublisher pattern: 'dependency-check-report.xml'
      }
    }
  }  

