# IB Gator (Interactive Brokers Gateway in Docker)

This repo creates a dockerized version of the latest IB Gateway. Build the image by running

```
sudo docker compose build --no-cache=true
```

You can start the container in the dev mode by running

```
sudo cp ./.env.dev ./.env && sudo cp ./docker-compose-dev.yml ./docker-compose.yml

```

Similarly, you can run the production container using

```
sudo cp ./.env.prod ./.env && sudo cp ./docker-compose-prod.yml ./docker-compose.yml

```
