pipeline {
  agent any
  stages {
    stage('paso1') {
      agent any
      steps {
        sh '''
pipeline {
    agent any

    stages {
        stage(\'Crear Documento\') {
            steps {
                script {
                    def currentDate = new Date()
                    def formattedDate = currentDate.format("yyyyMMdd_HHmmss")
                    def fileName = "documento_${formattedDate}.txt"

                    echo "Creando documento: ${fileName}"

                    writeFile file: fileName, text: "Hola mundo"
                }
            }
        }
    }

    post {
        success {
            echo "¡Tarea completada con éxito!"
        }
        failure {
            echo "La tarea ha fallado. Revisa los detalles."
        }
    }
}
'''
      }
    }

  }
}