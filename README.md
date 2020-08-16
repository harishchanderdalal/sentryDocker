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
    sentry:9.1.2 upgrade --noinput
 ```
 ```
 docker run -ti --rm \
    --network sentry_internal \
    -e SENTRY_SECRET_KEY=my_secret \
    -e SENTRY_POSTGRES_HOST=postgres \
    -e SENTRY_DB_USER=sentry \
    -e SENTRY_DB_PASSWORD=change_me \
    -e SENTRY_REDIS_HOST=redis \
    sentry:9.1.2 createuser
  ```
# How to generate SMTP Gmail Token
## Step 1
Log in to your Google account with your login credentials. First, enter your email address and click on Next button.
![Gmail](https://user-images.githubusercontent.com/22466745/90329668-7fdd1200-dfc4-11ea-972e-57f1deb4af2d.png)
![GPassword](https://user-images.githubusercontent.com/22466745/90329683-97b49600-dfc4-11ea-845c-f550db02a656.png)
![AppPass](https://user-images.githubusercontent.com/22466745/90329761-0691ef00-dfc5-11ea-9be5-eb0bf207056d.png)
![CPass](https://user-images.githubusercontent.com/22466745/90329763-08f44900-dfc5-11ea-9d1f-1a9ddb666b6a.png)
![G1](https://user-images.githubusercontent.com/22466745/90329765-0a257600-dfc5-11ea-83cb-e47d9dcba4ca.png)
![G2](https://user-images.githubusercontent.com/22466745/90329766-0abe0c80-dfc5-11ea-8f15-20102e00b9f6.png)
