---
layout: default
title: Post thread commands
---

You can easily define certain commands that Semaphore executes after the build commands on each thread, regardless of whether it passed or failed.

To set it up simply set a command to "Post-thread" in your project's Build Settings.

![Build settings](/assets/images/post-thread-commands.png)

This is great when you need to, for example, upload assets to S3 or tail the test.log when you're not sure why a certain spec or scenario failed.

There is also a new environment variable available to these commands: `SEMAPHORE_THREAD_RESULT`. It can hold the value of either "passed" or "failed".
