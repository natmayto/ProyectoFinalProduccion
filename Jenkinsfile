pipeline {
  agent any
  stages {
    stage('PIPELINE2') {
      steps {
        sleep(time: 2, unit: 'MINUTES')
        build(job: 'JOB-3', propagate: true)
        withSonarQubeEnv(installationName: 'jenkins-sonar', credentialsId: '9d4bce51552c86418c84e3fe7e58dd23746e4ecf', envOnly: true) {
          echo 'SonarQube'
        }

      }
    }

  }
}