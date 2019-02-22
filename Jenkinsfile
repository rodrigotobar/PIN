pipeline {
  agent any
  stages {
    stage('CheckOut') {
      parallel {
        stage('Descarga de Dependencias') {
          steps {
            sh 'ls'
            echo 'Paso correcto'
          }
        }
        stage('SCM Validacion Metodologia') {
          steps {
            sh 'ls'
          }
        }
      }
    }
    stage('Analysis') {
      parallel {
        stage('Sonarqube') {
          steps {
            sh 'ls'
          }
        }
        stage('SCM Validacion PU') {
          steps {
            registerWebhook()
          }
        }
      }
    }
    stage('Deploy to DEV') {
      steps {
        sh 'ls'
      }
    }
    stage('End') {
      steps {
        echo 'Pase Exitoso'
      }
    }
  }
}