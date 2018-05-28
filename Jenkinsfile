pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        cleanWs()
      }
    }
    stage('Download') {
      steps {
        echo 'Descargar'
      }
    }
    stage('Calidad') {
      steps {
        echo 'Calidad'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Desplegar en AWS'
      }
    }
  }
}