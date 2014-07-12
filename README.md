Creates a container that exposes port 5432 to allow other containers to use postgresql as a service.

available via

```
docker pull gdoteof/postgres
```

or build it
```
docker build -t postgres .
```

Link to another docker (for example, webapp)

```
docker run -d --name db postgres
docker run -P --name webapp --link db:db you/webapp
```


the created docker, webapp, can see the postgres server at tcp://db:5432


this build contains a postgres super user `docker` with password `docker` and a database called `docker`
