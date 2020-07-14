---
title: "Deploying Challenges"
description: "Automatic deployment of CTF challenge servers"
---

<div class="alert rounded-0 alert-primary">
  Automatic challenge deployment is only available to Hosted and Enterprise installations of CTFd
</div>

Automatic Challenge Deployment allows CTFd to manage and deploy Capture The Flag challenges in the form of challenge containers. Challenge containers are typical applications packaged using Docker into Docker images.

However challenge containers/services must have certain properties.

- Challenge containers must [EXPOSE](https://docs.docker.com/engine/reference/builder/#expose) a port (e.g. EXPOSE 8000) in their Dockerfile/image.
- Challenge containers should be as small as possible
- Challenge containers should not be comprised of multiple applications
- Challenge containers are not made with docker-compose

## Creating Services

To create a service based challenge:

1. Login as an administrator and navigate to the Admin Panel.
2. Click on the "Services" link on the top right
3. Click the plus icon to go to the create service page
4. Give your service a title in lowercase only and click the "Create" button
5. Build your docker image
6. After building the docker image, run the commands listed on the service page
   - docker login [ctfd.io]
   - docker tag [your built image][ctfd.io]
   - docker push [ctfd.io]/[your built image]
7. The service page will then update with the address and port of the challenge (You may need to manually refresh the page).

### Example of pushing docker image

```text
$ docker login demo.ctfd.io
Username:
Password:
Login Succeeded

$ docker tag challenge demo.ctfd.io/challenge

$ docker push demo.ctfd.io/challenge
The push refers to repository [demo.ctfd.io/challenge]
d331a460b7f1: Pushed
b826215d4ea3: Pushed
0987a4ff6d69: Pushed
d7a1c1d656bd: Pushed
2c77720cf318: Pushed
1f6b6c7dc482: Pushed
c8dbbe73b68c: Pushed
2fb7bfc6145d: Pushed
latest: digest: sha256:... size: 12345
```
