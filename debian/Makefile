build:
	docker build -t jupyterhub:v1 .

run: build
	docker run -it -p 18000:8000 -p 18001:8001 --name jupyterhub jupyterhub:v1

rm:
	docker rm jupyterhub -f