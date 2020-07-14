---
title: "Integrating With Major League Cyber"
description: "Integrate your CTFd instance with MajorLeagueCyber"
---

You can integrate CTFd with Major League Cyber as an OAuth provider.

To start off, create a new event on MajorLeagueCyber by following the event creation wizard. Be sure to select the User Mode for your event to be the same as your settings in CTFd.

![](/images/mlc/create-event.png)

On your event page, click the "Edit" button in order to get your integration details.

![](/images/mlc/edit-event.png)

Click on the "Integration" tab to get your details. In order to get OAuth with your CTFd instance working, fill in the redirect URL with your CTF URL + /redirect.

![](/images/mlc/integration.png)

In the config page of CTFd, be sure to enter the client ID and client secret from Major League Cyber.

![](/images/mlc/ctfd-config.png)

Now, people will be able to log in to CTFd using Major League Cyber!
