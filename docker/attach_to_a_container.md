# Attach to a Container

To attach to a running container in docker we can use the command exec 1st to set up a shell on the specified container.

```
docker exec -it "id of running container" bash
```

Which would then let us be able to modify the container in a bash shell. (Shouldnt do this in production)
