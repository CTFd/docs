---
title: "Email Settings"
---

## Email Content

CTFd allows administrators to configure the content sent out in emails. For example, an admin can configure the email sent out to new users to have additional registration instructions.

![](/images/config/email-content-settings.png)

Under the email tab in the Admin Panel Settings page you can customize the content of the email subject and body of the following emails:

 * New User Account Confirmation
 * New User Account Details
 * Password Reset
 * Password Reset Confirmation

Variables are injected into the emails before sending the email allowing you to further customize the content of emails.

 * <code>ctf_name</code> - contains the configured name of your CTFd instance
 * <code>ctf_description</code> - contains the configured description of your CTFd instance
 * <code>url</code> - contains the target URL of the email (e.g. forgot password link, account confirmation link)

To inject a variable use the format of:

<code>{variable}</code>

For example: <code>{ctf_name}</code>

## Email Server

<div class="alert rounded-0 alert-primary">
  Hosted CTFd instances are automatically configured to send email through our email providers. The default configured email to send mail from is "noreply@[subdomain].ctfd.io".
</div>

CTFd allows for admins to configure what email server they'd like to send emails through. This can be accessed from the email tab in the Admin Panel Settings page.

![](/images/config/email-server-settings.png)