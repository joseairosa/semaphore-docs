---
layout: default
title: How to securely add custom file
---

For your new custom file you need to specify a target file path. For instance, if you have a project "semaphore\_builder" and you want to add a new custom file to your project's config directory, your file path should look like the one on the screenshot below:

<img src="/assets/images/new-custom-file.png" alt="New custom file" style="width: 100%;"/>

Content of the new custom file can be entered in content text area.

For greater security, the content of your custom files can be encrypted. We strongly recommend that you select this option if you are adding sensitive content such as SSH keys. Once encrypted, encrypted file cannot be edited. The identity of your file can determined by an MD5 hash.

<img src="/assets/images/custom-file-list.png" alt="Custom file list" />
