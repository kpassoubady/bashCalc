pipeline {
  agent {
    node {
      label 'unix'
    }

  }
  parameters {
        string(name: 'USER_NAME', defaultValue: 'Kangs', description: 'Please enter your user name')
  }
  stages {
    stage('Start') {
      steps {
        sh 'echo starting the execution'
        // the below one used for scripted pipeline
        //properties([[$class: 'JiraProjectProperty'], [$class: 'ScannerJobProperty', doNotScan: false], gitLabConnection(''), [$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false], parameters([string(defaultValue: 'Kangs', description: 'Please enter your user name', name: 'USER_NAME', trim: false)]), [$class: 'ThrottleJobProperty', categories: [], limitOneJobWithMatchingParams: false, maxConcurrentPerNode: 0, maxConcurrentTotal: 0, paramsToUseForLimit: '', throttleEnabled: false, throttleOption: 'project']])
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
