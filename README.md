# Build the project
dotnet new razor -o aspnetcore-docker
cd aspnetcore-docker
dotnet run

# Create the Dockerfile

# Build the Docker image
docker build -t aspnetcore-docker:1.0 .

# Tag the image before push
docker tag aspnetcore-docker:1.0 danmgs/aspnetcore-docker:1.0

# Push the image to docker hub (public registry)
docker push danmgs/aspnetcore-docker:1.0