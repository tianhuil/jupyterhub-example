build:
	docker build -t jupyter:v1 .

run:
	docker run -it --name jupyter jupyter:v1

exec:
	docker exec -t jupyter sh

python:
	docker exec -t jupyter python3 --version

delete:
	docker rm jupyter -f
