---
layout: default
published: true
weight: 1
---

# Pre-Launch Config
Before launching a website, make sure to complete all of these steps for plugin config and other settings at least 1 day before launch.

## Add new website to Cloudflare
1. Log in to the Unity account on Cloudflare
2. Click "add a site" and enter the domain name without www
3. Follow the prompts and select the free plan
4. Confirm that the site has been added to Cloudflare

## Change nameservers  
1. Login to the domain registrar (you need to get this from the client)
2. Find the nameservers and remove the old ones
3. Point the domain to Cloudflare using the following nameservers:
`dean.ns.cloudflare.com`
`gail.ns.cloudflare.com`

## Set up Google Analytics
1. On the old website, right click and select "view page source"
2. Search the document (cmd-f on mac) for `UA`
3. Make sure of the tracking code (ex: UA-183747)
4. In the WordPress dashboard of the new site, go Settings > Google Analytics
5. Expand plugin settings and paste in tracking code
6. Uncheck "disable tracking" of admin level users

## Add Favicon
From the WordPress dashboard, go to Appearance > Customize > Site Identity. Upload an icon to use as the favicon. It should be at least 512 x 512px and square. Click Publish.

## Change Site Information
Run through the following to make sure contact information has been changed to the client's preferred email address.
- Contact Form 7
- Settings > General
- From Appearance > Customizer, make sure Site URL and Tagline are filled in
