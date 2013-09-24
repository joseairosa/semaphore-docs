---
layout: default
title: Integration with Cloud 66
---

[Cloud 66](https://www.cloud66.com) makes it easy to provision, deploy and manage your Ruby on Rails application on any cloud. Semaphore has native integration for deployment through Cloud 66.

1) Make sure your stack is deployed with Cloud 66. Learn more about [deploying Rails stacks with Cloud 66](https://www.cloud66.com/help/first_stack).

2) In Semaphore, go to your project setting and click on Deployment.

![Project settings](/assets/images/cloud66-integration/project_settings.png)

3) If you have no deployments configured, you can add your first server.

![Deployment settings](/assets/images/cloud66-integration/project_settings_deployment.png)

4) Select Cloud 66 from the list of Deployment Methods and choose Automatic.

![Deployment method](/assets/images/cloud66-integration/deployment_method.png)

5) You will be redirected to your Cloud 66 account and asked if you give Semaphore permission to deploy your stacks on your behalf.

![OAuth access between Semaphore and Cloud 66](/assets/images/cloud66-integration/oauth_access_rights.png)

6) Select the project you would like to deploy once the tests are successful.

Done!

Note that while Semaphore tracks every deploy in the project timeline, it sends a blank request to Cloud66 to perform the actual deployment work. If it fails for some reason, Cloud 66 will inform you.
