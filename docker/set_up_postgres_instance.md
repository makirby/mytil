# Set up postgres instance

On the ubuntu server download latest postgres docker image

```
docker pull postgres
```

Now we have the latest version of the official postgres image we can attach it to the locally running docker service. 

```
$ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```
This will also (-e) EXPOSE 5432, the default postgres port allowing concurrently running containers to link easily. The default (-d) postgres user and database are created with initdb as the entry point.

To connect another image/app that needs to use the original postgres container we have to run it with the below command.

```
$ docker run --name some-app --link some-postgres:postgres -d application-that-uses-postgres
```
