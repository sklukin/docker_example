istinpro:
	docker-compose up -d db
	docker-compose up -d loaddbistinpro
	docker rm -f loaddbistinpro
	docker restart db
	docker-compose up -d istinpro

rm:
	docker-compose stop
	docker-compose rm -f
