# Pre-Launch WP Settings & Config
Before launching a Simple site, make sure to complete all of these steps for plugin config and other settings at least 1 day before launch.

## Add new website to Cloudflare
1. Log in to the Unity account on Cloudflare
2. Click "add a site" and enter the domain name without www
3. Follow the prompts and select the free plan
4. Confirm that the site has been added to Cloudflare

## Change nameservers  
1. Login to the domain registrar (you need to get this from the client)
2. Find the nameservers and remove the old ones
3. Point the domain to Cloudflare using the following namerservers:
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


## Redirection Plugin by John Godley
Start the setup. Make sure the following are checked or unchecked.

[x] monitor permalink changes
[x] keep logs
[ ] store ip

Follow the prompts prompts

Go to Options > URL and select "monitor changes to posts"


## Security Safe Plugin by Sovereign Stack, LLC
### Privacy
[x] Hide WordPress version publicly
[x] Hide script version

### Files
#### Settings
[ ] All auto updates
[x] Disable theme editing

#### Core, Theme, Uploads, Plugins
Files should be 644, Directories should be 755
Make sure to click "update permissions" at the bottom of the page.

#### Access
[ ] Login errors
[x] Disable remote control

Add Google Search Console


## Autoptimize Plugin by Frank Goossens
Click "Show advanced settings"

#### CSS Options
[x] Optimize CSS Code
[x] Aggregate CSS-files
[x] Also aggregate inline CSS
[ ] Generate data: URIs for images
[ ] Inline and Defer CSS
[ ] Inline all CSS

#### HTML Options
[x] Optimize HTML Code
[x] Keep HTML comments

#### Misc Options
[x] Save aggregated script/css as static files
[x] Minify excluded CSS and JS files
[ ] Also optimize for logged in users


## The SEO Framework by Sybre Waaijer

### General Settings
#### Layout Tab
SEO Bar Settings
- [x] Display the SEO Bar in overview tables?
- [x] Display the SEO Bar in the SEO Settings metabox?

Counter Settings
- [x] Display pixel counters?
- [x] Display character counters?

#### Performance Tab

Query Alteration Settings
- [ ] Enable search query alteration?
- [ ] Enable archive query alteration?

Transient Cache Settings
- [x] Enable automated description output cache?
- [x] Enable automated Schema output cache?
- [x] Enable sitemap generation cache?

#### Canonical Tab

Scheme Settings: Detect automatically

Link Relationship Settings:
- [ ] Add rel link tags to Posts and Pages?
- [x] Add rel link tags to Archives?
- [x] Add rel link tags to the Home Page?

#### Timestamp Tab
Default is fine

### Title Settings

#### General Tab
Default is fine

#### Additions
Right

#### Prefixes
Default is fine

### Description Meta Settings

#### General Tab
default is fine

#### Additions
Both unchecked

### Home Page Settings

#### General Tab
Make sure Tagline and Description have keywords and they're not too long.

#### Additions
Left, add tagline

#### Robots
Uncheck all

#### Social
Screenshot top of home page

### Social Meta Settings

#### General Tab

- [x] Output Open Graph meta tags?
- [x] Output Facebook meta tags?
- [x] Output Twitter meta tags?

Add fallback image

- [ ] Output shortlink tag?

#### Facebook

Skip App ID
Add link to FB URL

#### Twitter

- [x] Summary large image

Add handle

#### Post Date

Both checked

### Schema Settings

#### Structure

- [x] Enable Breadcrumbs?
- [x] Enable Sitelinks Searchbox?

#### Presence

- [x] Output Authorized Presence?

An Organization and add their authorized name

Add logo: Make sure it's square

Add links to their Social Pages

### Robots Meta Settings

#### General
- [ ] Apply `noydir` to the entire site?
- [x] Apply `noindex` to every second or later archive page?

#### Indexing
All checked (except not entire site)

#### Following
All checked (except not entire site)

#### Archving
None checked

### Webmaster Meta Settings

Just Google and Bing.

### Sitemap Settings

#### General
- [x] Output sitemap?

#### Robots.txt
- [x] Add sitemap location in robots?

#### Timestamps
- [x] Add `<lastmod>` to the sitemap?

#### Ping
Check all

#### Style
- [x] Style Sitemap?
- [ ] Add site logo?

Choose on-brand colors. They must contrast enough with each other

### Feed Settings

- [x] Convert feed entries into excerpts?
- [x] Add link to source below the feed entry content?

## WP Fastest Cache Settings

Check the following:
 - Cache System Enable
 - Logged-in Users
 - New Post (Clear All Cache)
 - Update Post (Clear Cache of Post/Page)
 - Minify HTML
 - Minify CSS
 - Combine CSS
 - Gzip
 - Browser Caching
 - Disable Emojis
