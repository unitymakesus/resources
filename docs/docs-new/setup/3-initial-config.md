# Initial WordPress Settings & Config
These are the settings and steps steps you should take anytime a new WordPress website is set up.

1. Install and activate required plugins (see general > plugins).
2. Add API keys for Pro plugins to enable updates.
3. Update WordPress and plugins.

## Setting up content
1. Delete "Hello World!" post and empty trash.
2. Delete "Sample Page" page and empty trash.
3. Create new page, title it "Home" and hit publish.

## Media > WP Smush
1. Enable automatic smush
2. Enable full-size image resizing

## Settings > General
1. Site Title: [Client's name]
2. Remove Tagline. This will be set up before launch for optimal SEO.
3. Timezone: Set to client's timezone. Eastern Time is "New York," because this will automatically adjust for DST.
4. Week Starts On: Sunday

## Settings > Discussion
These settings will disable comments and completely prevent spam comments from being submitted by tricky bots.

1. Uncheck all "Default article settings."
2. Next to "Other comment settings," make sure *Users must be registered and logged in to comment* is checked.
3. Uncheck all "Email me whenever."
4. Next to "Before a comment appears," make sure *Comment must be manually approved* is checked.
5. Uncheck "Avatar Display."

## Settings > Excerpt
The length of the excerpt here depends on the individual website's design. For now, make sure the following settings are configured:

1. Check "Read More Link." The text that is here is determined by the individual website's design too.
2. Uncheck "No Custom Excerpts"
3. Uncheck "Filter: the_content()"
4. Strip Tags: Switch to "Remove all tags..." and don't check any boxes below.
