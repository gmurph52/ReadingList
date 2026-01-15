# ReadingList
This is in the start of a Go web service. I will be expanding this and adding a full API with a database and then a Web app.

## Project setup

### Database Setup
This is set up to work with a postgres DB. You will need to set up a postgres database with the correct schema.
  TODO: create a migration/script to set up correct schema.
Then set an environment varialbe name `READINGLIST_DB_DSN` with the DB connection string.
 e.g. `export READINGLIST_DB_DSN='postgres://readinglist:[your-password]@localhost/readinglist?sslmode=disable'`


### Start the app
```
 go run ./cmd/api/
```
