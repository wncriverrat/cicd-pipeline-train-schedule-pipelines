pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
    stage ('Test') {
      steps {
        echo "Run the automated tests"
        sh 'ls /tmp'
      }
    }
    stage ('Deploy') {
      steps {
        echo 'Doing the deploy'
        sh 'pwd;touch foo.txt;cp foo.txt /tmp'
      }
    }
  }
}
