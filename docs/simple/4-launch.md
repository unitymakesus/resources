---
layout: default
published: true
weight: 3
---

# Simple Launch
Follow these steps to launch a Simple site. Before going any further, make sure everything has been completed in the pre-launch config.

## On the Unity Server
- In the Just Get Simple cPanel
- Domains > create a new domain "sitename.com"

## On Cloudflare
- In the website account
- DNS > update A record to new IP: `209.124.90.253`

## On the new website dashboard
- Tools > Domain Mapping
- Add new domains for www and non www
- Make the primary domain their current one for SEO reasons

## On Simple My Sites > Network Admin dashboard
- Settings > Migrate DB Pro
- Find and Replace > Select specific sub site
  * Find: `//justgetsimple.com/sitename`
  * replace: `//www.siteurl.com` or `//siteurl.com`

## Clearing caches
- Settings > Beaver Builder > Tools > Clear Cache
- Autoptimize > Clear Cache

**When you are finished, go to a private browser and check all links and images to make sure everything works properly**
