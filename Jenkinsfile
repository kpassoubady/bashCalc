pipeline {
  agent {
    node {
      label 'Windows'
    }

  }
  stages {
    stage('RunHello') {
      steps {
        ansiColor(colorMapName: 'xterm') {
          sh './hello.sh'
        }

      }
    }
  }
}