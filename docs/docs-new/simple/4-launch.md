---
layout: default
published: true
order: 4
---

# Simple Launch
Follow these steps to launch a Simple site. Before going any further, make sure everything has been completed in the pre-launch config.

## On the new website dashboard
- Tools > Domain Mapping
- Add new domains for www and non www
- Make the primary domain their current one for SEO reasons

## Clearing caches
- Settings > Beaver Builder > Tools > Clear Cache
- Autoptimize > Clear Cache

## On Simple My Sites > Network Admin dashboard
- Settings > Migrate DB Pro
- Find and Replace > Select specific sub site
  * Find: `//justgetsimple.com/sitename` (ex: //justgetsimple.com/pphd)
  * replace: `//www.siteurl` or `//siteurl` (ex: //www.thepocketphd.com)

## On the Unity Server
- In the Just Get Simple cPanel
- Domains > create a new domain "sitename.com"

## On Cloudflare
- In the website account
- DNS > update A record to new IP: `209.124.90.253`

**When you are finished, go to a private browser and check all links and images to make sure everything works Properly**
