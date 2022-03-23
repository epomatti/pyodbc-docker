# Docker pyodbc + mssql

An image with pyodbc for Microsoft SQL Server.

```sh
docker pull epomatti/pyodbc-mssql:latest
```

### Testing

Small application for testing the image configuration:

```sh
cp config.dev.ini config.ini

docker-compose build
docker-compose up
```

### Docker Hub

Commands for manually publishing the image to Docker Hub:

```sh
export dockerHubImage='epomatti/pyodbc-mssql:latest'

docker image build -t pyodbc-mssql:latest ./image
docker login --username='<username>'
docker tag '<image_id>' $dockerHubImage
docker push $dockerHubImage
```