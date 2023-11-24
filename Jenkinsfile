pipeline {
  agent any
  stages {
    stage('paso1') {
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
                    
                    // Imprimir la ubicación del archivo creado (opcional)
                    echo "Archivo creado: ${fileName}"
                    
                    // Mover el archivo a otra carpeta
                    bat "move ${fileName} ruta\\\\carpeta_destino\\\\${fileName}"
                    // o para sistemas Unix:
                    // sh "mv ${fileName} ruta/carpeta_destino/${fileName}"
                }
            }
        }
    }
}'''
        }
      }

    }
  }