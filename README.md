# ReadingList
A Go webservice used for creating and updating a reading list.
This is a full Go web service with a postgreSQL database and a Go web app. The web app is still in progress.

## Project setup

### Database Setup
This is set up to work with a postgres DB. You will need to set up a postgres database with the correct schema.

With docker
```
docker pull postgres
docker images | grep postgres // verify the image is there

// first time
docker run --name reading-list-db-container -e POSTGRES_PASSWORD=[password] -d -p 5432:5432 postgres // create container, env var for password, expose port, and use postgres image
or 
docker run -d --name reading-list-db-container -e POSTGRES_DB=readinglist -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=password -v pgdata:/var/lib/postgresql -p 5432:5432 postgres // create container, env var for password, expose port, and use postgres image, and persist database
// after first time
docker start reading-list-db-container

docker ps // verify postgres is running
docker exec -it reading-list-db-container psql -h localhost -p 5432 -U postgres // connect to DB

```

  TODO: create a migration/script to set up correct schema.
Then set an environment varialbe name `READINGLIST_DB_DSN` with the DB connection string.
 e.g. `export READINGLIST_DB_DSN='postgres://readinglist:[your-password]@localhost/readinglist?sslmode=disable'`


### Web Service 
A web service written in Go

## Start the app
```
 go run ./cmd/api/
```

### Web App
A web app written in Go

## Start the app
```
 go run ./cmd/web/
```

