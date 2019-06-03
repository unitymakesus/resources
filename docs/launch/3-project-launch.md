---
layout: default
published: true
weight: 3
---

# Project launch
Follow these steps to launch a website site. Before going any further, make sure everything has been completed in the pre-launch config and plugins.

## Find and Replace Database
- Tools > Migrate DB Pro
- Find and Replace
  * Find: `//sitename.beta.unitymakes.us/`
  * replace: `//www.siteurl.com` or `//siteurl.com`

## Change Site URL
- Login to the Unity (WHM account)[https://server.unitymakes.com:2087/]
- Go to Account Functions > Modify an Account   
- Find the beta site and click "modify"
- Change the primary domain to `siteurl.com`
- Click save
- Scroll to the bottom of the page and click "Back to list accounts"

## Adding SSL Certificate
- From the new account, click the cPanel icon
- Go to Security > SSL/TLS
- Click link under Certificates (CRT)
- Scroll to "Generate a New Certificate":
    - Key: Default
    - Domains: `sitename.com`
               `*.sitename.com`
    - City: Client city
    - State: Client state
    - Country: US
    - Company: client name
    - Passphrase: empty
- Click generate
- Scroll to bottom of the page and click "Return to SSL/TLS page"
- Scroll to "Install and manage SSL"
- Install an SSL Website > select domain
- Click "Autofill by Domain"
- Click "Install Certificate"

## Set Email SPF Records
### From the WHM cPanel
- Go back to the cPanel dashboard
- Email > Email Deliverability
- Click "manage"
- Copy the DKIM value

## From Cloudflare
- Find the account and go to DNS
- Add a TXT Record with the following:
    - Name: `default._domainkey`
    - Click to configure: paste value from DKIM
- Click "Add Record"

DOMAIN SETTINGS
additional hosts: server.unitymakes.com

PREVIEW OF UPDATED RECROD
copy string

In Cloudflare, DNS find txt with v=spf1 in value
paste string and click udpate

## Point A Record in Cloudflare
- DNS > update A record to new IP: `209.124.90.253`
- Check site to make sure it worked

## Check Crypto in Cloudflare
- Crypto > Make sure Edge Certificate exists
- Toggle on "Always use HTTPS"
- Toggle on "Automatic HTTPS Rewrites"

**When you are finished, go to a private browser and check all links and images to make sure everything works properly**
