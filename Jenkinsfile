pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Build Success'
      }
    }

    stage('Test') {
      parallel {
        stage('Test Stages') {
          steps {
            echo 'Test2 Succes'
          }
        }

        stage('Test1') {
          steps {
            echo 'Test1 Success'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Depoly or not', ok: 'Yes,i\'m sure')
        echo 'Deploy Succes'
      }
    }

  }
}