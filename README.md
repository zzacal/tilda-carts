## What is it?
It's a way to fake cart service. This is to allow developers to make calls to a fake cart service while working on the payment ui.

## Requirements
1. [Docker Desktop](https://docs.docker.com/desktop/install/mac-install/) or [Docker Engine](https://docs.docker.com/engine/install/)

## Starting the container
1. start docker engine or docker desktop
1. start the container
   ```sh
   docker compose up -d
   ```

## Setting up payment ui
1. point to the fake cart service using this env: AWPS_URL="http://localhost:8110/"
1. start payment ui
1. navigate to `http://localhost:3000/transaction/some-fake-cart/` 
1. you got it!
  - ![](./Screen%20Shot%202023-09-28%20at%204.40.03%20PM.png)

## How does it work?
[tilda](https://hub.docker.com/repository/docker/jizacal/tilda/general) is a web service faking tool that can be configured to respond to requests in any way you want. The `seed.json` file contains a configuration for a request to "/cart/some-fake-cart". tilda will respond to that request as configured.
