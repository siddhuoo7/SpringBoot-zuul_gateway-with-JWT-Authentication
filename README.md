# SpringBoot-zuul_gateway-with-JWT-Authentication

This Code authenticate all the Request from the user , inorder to get the response we must provide a jwt token 

Crete a Eureka server and Register all the client application to eureka server 

eureka server ip and zuul routes must be provide in application.yaml

created a hello endpoint while calling normally it shows error lets do the following steps to get the resp 

Login using HTTP Basic ,Using postman or any Rest client give the Post request to the given url 

```shell
Request url
http://localhost:8556/authenticate

Request body
{"username":"admin",
"password":"admin1$"}

```

Inspect the response contents and find the authorization header. 
It should look like:

```shell
 jwt: eyJhbGciOiJIUzI1Ni.....
```

Use this as Authorization in another request header  append "Bearer " in front of the token:

```shell
Request url
localhost:8556/hello

Request header
Authorization:  Bearer eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsImV........
```

You should be able to consume the API

### That's all

Hope you enjoy it.
