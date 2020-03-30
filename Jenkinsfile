pipeline {
  agent {
    node {
      label 'unix'
    }

  }
  stages {
    stage('RunHello') {
      steps {
        ansiColor(colorMapName: 'xterm') {
          sh 'bash ./hello.sh'
        }

      }
    }
  }
}
