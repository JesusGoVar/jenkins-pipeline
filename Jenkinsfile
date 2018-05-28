pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        //cleanWs()
        echo 'Limpiar'
      }
    }
    stage('Build') {
      steps {
        sh 'su docker build -t app .'
      }
    }
    stage('Download') {
      steps {
        echo 'Descargar'
      }
      post{
        always{
          echo 'esto siempre sale'
        }
        failure{
          echo 'Mandar correo'
        }
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