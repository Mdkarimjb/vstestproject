pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        build(job: 'test', propagate: true, quietPeriod: 2, wait: true, waitForStart: true)
        echo 'successfully build'
      }
    }

  }
}