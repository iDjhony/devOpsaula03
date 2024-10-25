pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		
		
	# Iniciar o Backend (Flask) e Frontend
	echo "Iniciando o backend Flask..."
	cd $DIR

	rm -rf devops

	# firefox index.html

	python3 -m venv devops

	# Ativar o ambiente virtual
	source devops/bin/activate

	pip install flask

	pip install flask-cors

            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
		# Rodar a aplicação Flask
		python3 main.py --host=0.0.0.0 &

		echo "Backend e Frontend estão rodando

            }
        }
    }
}

