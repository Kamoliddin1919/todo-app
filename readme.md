* How to run the project?
```azure
go run cmd/main
```
* How to run postgres using docker?
```azure
 docker run --name=todo-db -e POSTGRES_PASSWORD='your_password' -p 5436:5432 -d --rm postgres
```
* How to create migrate?
```azure
migrate create -ext sql -dir ./schema -seq init
```
* How to run migrate?
```azure
migrate -path ./schema -database 'postgres://postgres:your_password@localhost:5436/postgres?sslmode=disable' up 
```
* How to install swagger?
```azure
go install github.com/swaggo/swag/cmd/swag@latest
```
* How to init swagger?
```azure
swag init -g cmd/main.go 
```