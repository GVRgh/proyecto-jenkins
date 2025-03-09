pipeline  {
	agent any

	stages {
		stage('Checkout') {
			steps {
				git url: ' https://github.com/GVRgh/proyecto-jenkins.git', branch: 'main'
			}
		}

		stage('Build') {
			steps {
				echo 'Compilando código...........'
				sh 'echo "Etapa Build exitosa" '
			}
		}

		stage('Test') {
			steps {
				echo 'Ejecutando pruebas automatizadas...........'
				sh 'echo "Etapa Test completada exitosamente" '
			}
		}

		stage('Deploy Simulation') {
			steps {
				echo 'Simulando Despligue...........'
				sh 'echo "Etapa Deploy Simulation exitosa" '
			}
		}
	}
}