pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        echo 'coucou'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
        bat(script: '"C:\\Program Files (x86)\\SmartBear\\SoapUI-5.4.0\\bin\\testrunner.bat" -j -c "Add TestCase" calculator-soapui-project.xml', returnStdout: true)
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
  post {
    always {
      junit '**/TEST-*.xml'

    }

  }
}