pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        //cleanWs()
        sh 'whoami'
      }
    }
    stage('Build') {
      steps {
        withCredentials([usernameColonPassword(credentialsId: 'ubuntu_jenkins', variable: 'ubuntu_jenkins')]) {
          // some block
          sh 'docker build -t app .'
        }
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