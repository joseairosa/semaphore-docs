---
layout: default
title: How to deploy to Heroku
---

With Semaphore it's very easy to set up continuous deployment process to your Heroku instance. To do that you only need to make sure that you have a configured server on Heroku and a corresponding project added to Semaphore.

To get started, go to your project's settings > Deployment and click to add a new server. This will launch a simple process that consists of 4 steps.

- Choosing your deployment strategy
- Providing Heroku API token
- Choosing Heroku application
- Naming your server on Semaphore


## Choosing your deployment strategy

There are two deployment strategies on Semaphore, "automatic" and "manual".
Automatic means that after every passed build on selected branch  will trigger deploy, of course beside that you can trigger deploy manually at any time.
Manual strategy offers you only manual way of triggering deploys.

## Providing Heroku API token

By providing your Heroku API token, you authorize Semaphore to configure SSH keys needed for deployment. You can find your API token under [account information](https://dashboard.heroku.com/account) on Heroku .


## Choosing the target Heroku application

After you select your application from the list, Semaphore will generate a new pair of SSH keys:

- Private key that will be encrypted and stored at Semaphore side
- Public key that will be added to your Heroku application's deploy keys.

## Naming your server on Semaphore

This is can be any name you like. It will be used on your Semaphore dashboard and deployment timeline.

By this point the setup is complete - you are ready to continuously deploy to Heroku.

If your application requires some additional deploy commands (such as running migrations after deploy) you can edit the default commands on the summary page or in project settings under "Deployment" tab.

**Note:** Semaphore platform includes the [Heroku toolbelt](https://toolbelt.heroku.com) and you can run any heroku command in your deployment process.