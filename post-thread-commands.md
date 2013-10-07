---
layout: default
title: Post-thread commands
---

You can easily define commands for Semaphore to execute after build commands on each thread, regardless of whether the build commands passed or failed.

To do this, simply set a command to "Post-thread" in your project's [Build Settings](/custom-build-commands):

![Build settings](/assets/images/post-thread-commands/settings.png)

This is useful when you need to, for example, upload assets to S3 or tail the test.log.

During these commands an [environment variable](/available-environment-variables) `SEMAPHORE_THREAD_RESULT` is available. It can hold the value of either "passed" or "failed".
