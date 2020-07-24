---
title: "Getting Started"
description: "Setting up your CTFd instance"
---

## Starting CTFd

After navigating to CTFd (http://localhost:8000 or http://localhost:4000 by default), you will see a setup page where you can choose the name of your Capture The Flag and the credentials for the first admin user.

![Setup Page](/images/setup/ctfd-setup-page.png)

## Setting Up

Upon creating the admin account, you will be redirected to the default home page. To setup your CTF further you will need to access the admin panel from the top right.

![Link to the Admin panel](/images/setup/admin-link.png)

From the admin panel we can create our first challenge and also configure attributes like when to open the CTF to competitors and when to end the CTF.

## Adding Your First Challenge to CTFd

From the admin panel, click on the Challenges link in the navigation bar.

Then click on the **New Challenge** <i class="fas fa-plus-circle"></i> button near the top of the page.

You should see something similar to the following image:

![Create Challenge Menu](/images/challenges/create-challenge-form.png)

Here you can give your challenge:

* a name
* a point value
* a description
* add any associated files
* and a flag.

Static flags are flags which are compared to the user's answer. If a user's answer matches your flag the user is marked correct.

Regex flags are flags which are compared using a regular expression. CTFd's regular expressions are always case insensitive. To test your regular expressions you can use the [pythex website](https://pythex.org/).

Static and regex flags can be marked case insensitive or not depending on how you want to process user input.

Once you're ready click the **Create** button at the bottom of the page.

If you didn't choose to hide your challenge and the CTF has started, your challenge is now visible to users.

## Adding New Pages to CTFd

CTFd allows you to create new pages using the **Pages** feature. To access it, click the Pages dropdown in the navigation bar and select **All Pages**.

By clicking the **Add Page** <i class="fas fa-plus-circle"></i> button, you will be taken to the page editor.

![Pages Functionality](/images/pages/pages-editor.png)

From here you will be able to add custom HTML or Markdown content to pages that users will be able to access.

From here you can specify the content of the page and the route where the page will be accessible.

The content can be written in Markdown or HTML and the route will be accessible by `/<route>` where `<route>` is the endpoint you specify (e.g. wiki, faq, news).

If you need to add files to your page (photos, videos, source code files, etc.) you can use the Media Library to upload any file you need to.

![Pages Media Library](/images/pages/media-library.png)

Once a file is uploaded, links can be added to it from the Page content.

## Saving your CTF

CTFd also supports importing and exporting CTFs allowing you to reuse the content you've written for one CTF into another. This can be very useful for saving team information, challenges, or configuration values.

To import/export a CTF from the admin panel, you can visit the **Config** page and click on the **Backup** tab as shown below:

![CTFd Backups](/images/export/ctfd-export-config.png)

From here you can click the export button to export the selected information into a zip file.

Conversely, you can click the **Import** tab to import a saved zip file.