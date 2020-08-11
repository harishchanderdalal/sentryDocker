# sentryDocker
Docker Stack Swarm

```
docker stack deploy -c sentry.yml sentry
```

```
docker run -ti --rm \
    --network sentry_internal \
    -e SENTRY_SECRET_KEY=my_secret \
    -e SENTRY_POSTGRES_HOST=postgres \
    -e SENTRY_DB_USER=sentry \
    -e SENTRY_DB_PASSWORD=change_me \
    -e SENTRY_REDIS_HOST=redis \
    sentry:8.22 upgrade --noinput
 ```
 
 ```
 docker run -ti --rm \
    --network sentry_internal \
    -e SENTRY_SECRET_KEY=my_secret \
    -e SENTRY_POSTGRES_HOST=postgres \
    -e SENTRY_DB_USER=sentry \
    -e SENTRY_DB_PASSWORD=change_me \
    -e SENTRY_REDIS_HOST=redis \
    sentry:8.22 createuser
  ```  
