# ReadingList
A Go webservice used for creating and updating a reading list.
This is a full Go web service with a postgreSQL database and a Go web app. The web app is still in progress.

## Project setup

### Database Setup
This is set up to work with a postgres DB. You will need to set up a postgres database with the correct schema.
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

