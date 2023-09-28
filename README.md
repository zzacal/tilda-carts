## What is it?
It's a way to fake cart service. This is to allow developers to make calls to a fake cart service while working on the payment ui.

## Requirements
1. [Docker Desktop](https://docs.docker.com/desktop/install/mac-install/) or [Docker Engine](https://docs.docker.com/engine/install/)

## Usage
1. start docker engine or docker desktop
1. start the container
   ```sh
   docker compose up -d
   ```
1. start payment ui
1. navigate to `http://localhost:3000/transaction/some-fake-cart/` 
1. you got it!
  - ![](./Screen%20Shot%202023-09-28%20at%204.40.03%20PM.png)