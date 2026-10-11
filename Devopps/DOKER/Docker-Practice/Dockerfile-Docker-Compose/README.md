# Build and run:

docker build -t hello-app .
docker run -d -p 5000:5000 hello-app


Visit http://localhost:5000

#  Data and volumes
# Containers are disposable. When you delete one, everything inside it is gone. For data you want to keep (like a database), use a volume:

docker run -d --name db -e POSTGRES_PASSWORD=secret \
  -v mydata:/var/lib/postgresql/data postgres:17

  # For development, a bind mount links a folder from your computer so code changes show up instantly:





  docker compose up -d      # start everything
docker compose logs -f    # watch logs
docker compose down       # stop and remove