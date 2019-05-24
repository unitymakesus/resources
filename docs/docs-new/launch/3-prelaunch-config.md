# Pre-Launch Settings & Confirg

## Plugins To Add Before Launch
* [Redirection](https://wordpress.org/plugins/redirection/)
* [Security Safe](https://wordpress.org/plugins/security-safe/)
* [The SEO Framework](https://wordpress.org/plugins/autodescription/)
* [WP Fastest Cache](https://wordpress.org/plugins/wp-fastest-cache/)

## Redirection Settings
Add redirects for all pages on the old site whose slugs have changed on the new site.

Monitor changes to posts and pages.

Set URL monitor changes to save to Modified Posts group.

Input file path for .htaccess file: `/home/[account]/public_html/.htaccess`

Edit "Redirections" Group to use Apache Module.

## Security Safe Settings

### Privacy
- [x] Hide WordPress Version
- [x] Hide Script Versions
- [ ] Make Website Anonymous

### Files
#### Settings
Uncheck all updates

- [x] Disable Theme Editing

#### Core, Theme, Uploads, Plugins

Files should be 644, Directories should be 755

### Access
- [x] Make login errors generic.
- [ ] Disable Password Reset
- [ ] Disable Remember Me Checkbox
- [x] Disable Remote Control
- [ ] Only Allow Local Logins

## The SEO Framework Settings
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
