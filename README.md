# IB Gator (Interactive Brokers Gateway in Docker)

This repo creates a dockerized version of the latest IB Gateway. Build the image by running

```
sudo docker compose build --no-cache=true
```

You can start the container in the dev mode by running

```
sudo cp ./.env.dev ./.env && sudo cp ./docker-compose-dev.yml ./docker-compose.yml && sudo docker compose up

```

Similarly, you can run the production container using

```
sudo cp ./.env.prod ./.env && sudo cp ./docker-compose-prod.yml ./docker-compose.yml && sudo docker compose up

```

## Read-only mode

Logging in the live/paper accounts for trading purposes requires the IB client to have the proper permissions.
Therefore, it is important to make sure that the connection is made without read-only permissions, that is, change in `config.ini`

```
ReadOnlyApi=no
```
and modify

```
ReadOnlyLogin=no
```
in `IBController.ini` and rebuild the docker image. You should be able to place/cancel orders, download trade statuses, and etc. 

