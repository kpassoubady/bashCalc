pipeline {
  agent {
    node {
      label 'unix'
    }

  }
  stages {
    stage('GatherInput') {
      steps {
        properties([[$class: 'JiraProjectProperty'], [$class: 'ScannerJobProperty', doNotScan: false], gitLabConnection(''), [$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false], parameters([string(defaultValue: 'Kangs', description: 'Please enter your user name', name: 'USER_NAME', trim: false)]), [$class: 'ThrottleJobProperty', categories: [], limitOneJobWithMatchingParams: false, maxConcurrentPerNode: 0, maxConcurrentTotal: 0, paramsToUseForLimit: '', throttleEnabled: false, throttleOption: 'project']])
      }
    }
    stage('RunHello') {
      steps {
        ansiColor(colorMapName: 'xterm') {
          sh 'bash ./hello.sh'
        }

      }
    }
  }
}
