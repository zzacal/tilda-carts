## What is it?
It's a way to fake cart service. This is to allow developers to make calls to a fake cart service while working on the payment ui.

## Requirements
1. [Rancher Desktop](https://rancherdesktop.io/). 
   - **IMPORTANT** Docker Desktop may be deprecated by the org in march. If you already have Docker Desktop, follow the [official migration guide](https://github.com/Alaska-ITS/EA-LivingDocuments/blob/main/RancherDesktop/InstallRancherDesktop.md).

## Starting the container
1. start Rancher Desktop
1. start the container
   ```sh
   docker compose up -d
   ```

## Setting up payment ui
1. point to the fake cart service using this env: AWPS_URL="http://localhost:8110/"
1. start payment ui
1. navigate to `http://localhost:3000/transaction/fake-cart/` 
1. you got it!
  - ![](./Screen%20Shot%202023-09-28%20at%204.40.03%20PM.png)

## Cart IDs
1. cart-200 - cart returns a 200
1. cart-404 - cart returns a 404
1. cart-500 - cart returns a 500
1. purchase-200 - cart returns 200; purchase returns 200
1. fake-cart

## How does it work?
[tilda](https://github.com/zzacal/tilda) is a web service faking tool that can be configured to respond to requests in any way you want. The directory `seeds/` contains fake responses from the payment service.