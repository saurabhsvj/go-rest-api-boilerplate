# go-rest-api-boilerplate
Boiler plate for developing a go lang based REST API with commonly used open source libraries


### Boilerplate Run instructions:
###### Note: Make sure your go environment is correctly setup for development.

Run the below commands in order on commandline
```python
# Install the glide package manager
curl https://glide.sh/get | sh

# Clone the boilerplate project
git clone https://github.com/sjoshi6/go-rest-api-boilerplate.git

cd go-rest-api-boilerplate

# (Optional) Update local dependencies to latest ( Do this if there is an error downloading a dependency)
glide update

# Installs all dependencies in project vendor folder.
glide install

# builds the application and creates a binary go-rest-api-boilerplate
go build

# Run the API server
GO_ENV_PORT=8000 ./go-rest-api-boilerplate
```

OR
Run the following docker commands
```python
cd go-rest-api-boilerplate

# Build the docker image
docker build -t go-boilerplate .

# Run the API in a container. Replace <free_port_on_host> with 8000
docker run -p <free_port_on_host>:8000 go-boilerplate
```

### Check the API output
```
curl http://localhost:8000/v1/users/1
```
Expected Output:
```
{"ID":0,"CreatedAt":"0001-01-01T00:00:00Z","UpdatedAt":"0001-01-01T00:00:00Z","DeletedAt":null,"age":35,"first_name":"bruce","last_name":"wayne"}
```
===================================================================================
```
curl http://localhost:8000/v1/users
```
Expected Output:
```
[{"ID":0,"CreatedAt":"0001-01-01T00:00:00Z","UpdatedAt":"0001-01-01T00:00:00Z","DeletedAt":null,"age":35,"first_name":"bruce","last_name":"wayne"},{"ID":0,"CreatedAt":"0001-01-01T00:00:00Z","UpdatedAt":"0001-01-01T00:00:00Z","DeletedAt":null,"age":35,"first_name":"batman","last_name":""}]
```
