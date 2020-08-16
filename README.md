# SentryDocker
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

Now, input your login password and click on the Next button again.
![GPassword](https://user-images.githubusercontent.com/22466745/90329683-97b49600-dfc4-11ea-845c-f550db02a656.png)

## Step 2
Now, you need to make sure that your Google account is well protected to avoid any intervention when using the SMTP service; therefore, we recommend enabling the 2-step verification offered by Google. If you have already enabled the 2-step verification, then you may jump to Step# 3.

## Step 3,a
Now, you need to generate an App Password which will be used as well for the SMTP integration, so  Click Here to visit the Google App Passwords page to generate an App Password.
![AppPass](https://user-images.githubusercontent.com/22466745/90329761-0691ef00-dfc5-11ea-9be5-eb0bf207056d.png)

## Step 3,b
Then, select app from the drop-down choice and choose Other (Custom name).
Log in to your Google account with your login credentials. First, enter your email address and click on Next button.
![CPass](https://user-images.githubusercontent.com/22466745/90329763-08f44900-dfc5-11ea-9d1f-1a9ddb666b6a.png)

## Step 3,c
Give any name of your choice to your App password and click on GENERATE button. In this example, we are naming this app password as Business email.
![G1](https://user-images.githubusercontent.com/22466745/90329765-0a257600-dfc5-11ea-83cb-e47d9dcba4ca.png)

## Step 4
Log in to your Google account with your login credentials. First, enter your email address and click on Next button.
![G2](https://user-images.githubusercontent.com/22466745/90329766-0abe0c80-dfc5-11ea-8f15-20102e00b9f6.png)
