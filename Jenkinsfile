pipeline {
  agent any
  stages {
    stage('paso1') {
      agent any
      steps {
        sh '''pipeline {
    agent any

    stages {
        stage(\'Crear Archivo\') {
            steps {
                script {
                    def fecha = new Date().format("yyyy-MM-dd-HH-mm-ss")
                    def fileName = "${fecha}.txt"
                    
                    // Crear el archivo con el contenido deseado
                    writeFile file: fileName, text: "Hola Mundo"
                    
                  
            }
        }
    }
}'''
        }
      }

    }
  }