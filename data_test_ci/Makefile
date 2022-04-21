up:
	sudo docker-compose --env-file ./env up --build -d

down: 
	sudo docker-compose down

shell:
	sudo docker exec -ti runner bash

format:
	sudo docker exec runner python -m black -S --line-length 79 .

isort:
	sudo docker exec runner isort .

pytest:
	sudo docker exec runner pytest /code/test

type:
	sudo docker exec runner mypy --ignore-missing-imports /code

lint: 
	sudo docker exec runner flake8 /code

ci: isort format type lint pytest
