---
title: "Hosted Subdomains and Custom Domains"
---

# Hosted Subdomains

Hosted CTFd instances are automatically provisioned with a subdomain
chosen by the creator. For example: `[domain].ctfd.io`. Instances will
be available by default on their hosted subdomain.

All hosted CTFd instances can use a custom domain (e.g.
`ctf.domain.com`). Setup instructions for custom domains are available
below.

Because of infrastructure requirements, hosted subdomains cannot be
disabled or changed. In addition, subdomains cannot be reserved for any
users without having an instance active.

# Setting up a Custom Domain

Hosted CTFd instances support the setting of a custom domain which your
instance will be accessible at including the `.ctfd.io` subdomain chosen
during the creation of the instance.

<div class="alert alert-warning">
    If you wish to have your instance at the root or apex domain (that is,
    at example.com instead of ctf.example.com), you may need to switch DNS
    providers to a DNS provider that supports <a href="https://blog.cloudflare.com/introducing-cname-flattening-rfc-compliant-cnames-at-a-domains-root/">CNAME Flattening</a>,
    <a href="https://blog.dnsimple.com/2011/11/introducing-alias-record/">ALIAS</a> records, or <a href="https://www.dnsmadeeasy.com/services/anamerecords/">ANAME records</a> first.
</div>

To set this custom domain use the following instructions:

1.  Go to <https://cloud.ctfd.io/admin> to see all hosted CTFd instances
    you have deployed
2.  Select your chosen instance and click the blue gear icon on the
    right.

![image](../../../images/hosted/domains/domain-blue-gear.png)

3.  Follow the instructions provided to set your custom domain to a
    CNAME of your `*.ctfd.io` subdomain. You will need to set the custom
    domain CNAME setting at your domain's DNS provider. The custom
    domain will not be set until the CNAME setting is properly
    configured and active.

    <div class="alert alert-warning">
        If you are using Cloudflare as your DNS provider you should not
        enable the Cloudflare proxy (e.g. the orange cloud). Cloudflare
        proxying can cause hosted CTFd systems to have difficulties in
        provisioning SSL certificates and identifying user IP addresses.
    </div>

    ![image](../../../images/hosted/domains/domain-setting-input.png)

4.  Once your domain is set, you can still access your CTFd instance
    through the `*.ctfd.io` subdomain. To remove or change your domain
    please contact us.
