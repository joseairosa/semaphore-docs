---
layout: default
title: Deploying with Capistrano
---

Nowadays Capistrano is important part of many teams workflows, tool wich provides seamless and easy deployment process. To use Capistrano with Semaphore you only need to make sure that you have a configured project that uses Capistrano as deployment method.

To get started, go to your project's settings > Deployment and click to add a new server. This will launch a simple process that consists of 4 steps.

- Choosing your deployment strategy
- Defining deploy commands
- Adding private SSH key for deploy
- Naming your server on Semaphore


## Choosing your deployment strategy

There are two deployment strategies on Semaphore, "automatic" and "manual".
Automatic means that after every passed build on selected branch  will trigger deploy, of course beside that you can trigger deploy manually at any time.
Manual strategy offers you only manual way of triggering deploys.

## Defining deploy commands

Defining custom deploy commands gives you ability to name your  deploy steps which will match your setup needs.

## Adding private SSH key for deploy

Best approach to handle permissions for your deployment process is to create separate SSH keys specifically for Semaphore deployment.
Generate new key pair with "ssh-keygen -t rsa" command and than add private key to Semaphore.
The public key should be added on your server, in the `.ssh/authorized_keys` file, inside the deploy user’s home directory. This key combination gives Semaphore permission to SSH inside the server and execute deploy process.

**Note:** Private key will be encrypted on Semaphore side and it will be available during deployment process, after initial setup there is no way to change it trough Semaphore interface.

## Naming your server on Semaphore

This is can be any name you like. It will be used on your Semaphore dashboard and deployment timeline.

By this point the setup is complete - you are ready to continuously deploy to your servers.