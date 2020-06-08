Changelog:

RC 3.0
- i.A.

2.9.1 Fix #1
- fixed xml summary output with summary_xml
- fixed rendering for set: home.html,home-sidebar.html
- change: classes/episode.php for summary output
- change: new var "summary_xml"; for correct feed output in tag itunes:summary
- new: summary is now enabled for markdown
- update demo 001.epi file

2.9 Extensions and QuorX 3 changes
- fixed PHP 7.2 and 7.3 changes (string to array)
- extension: disqus
  - fixed js,
  - hooks
  - new layout
  - isqus create infobox in QuorX 3 style
- pages: Netiquette for disqus link
- fixed full width for webplayer
- extension: contributors
  - delete google+
  - create mastodon
- QuorX3
  - navi: social links as blank target
  - navi: new social icon mastodon
  - js icon callback with mastodon
  - mastodon style icon
  - delete styles for webplayer
  - delete styles for subscribe button
  - delete middle container in set
  - change dict for translation (de)
  - delete old admin translation

2.8 PHP fixes for 7.x and new Attributes + QuorX 3
- fixed PHP 7.0 (eazy)
- fixed PHP 7.3 (mccouman)
- fixed webplayer extension
- new QuorX 3 Skin
  - style guides
  - theme functions
  - more hooks
  - contributors view (guest,podcaster)
- new meta types: feedattr_default
  - 'subtitle',         # Update for podlove webplayer
  - 'street',           # Impressum (required fields)
  - 'city',             # Impressum (required fields)
  - 'country',          # Impressum (required fields)
  - 'phone',            # Impressum (required fields)
  - 'fax',              # Impressum (required fields)
  - 'tax',              # Impressum (required fields)
  - 'image',            # QuorX 3 Skin style (required fields)
  - 'imageLicense',     # QuorX 3 Skin style (optional)
  - 'imageCreator',     # QuorX 3 Skin style (optional)
  - 'imageURL',         # QuorX 3 Skin style (optional)
  - 'supporter'         # Sidebar project support (optional)
- new meta types: itemattr
  - 'subtitle',         # Update podlove webplayer / xml
  - 'summary',          # Update for podlove webplayer
  - 'banner',           # QuorX 3 Skin style (optional)
  - 'bannerLicense',    # QuorX 3 Skin style (optional)
  - 'bannerPage',       # QuorX 3 Skin style (optional)
  - 'bannerURL',        # QuorX 3 Skin style (optional)
  - 'image',            # QuorX 3 Skin style (optional)
  - 'intro',            # QuorX 3 Skin style (optional)
  - 'outro',            # QuorX 3 Skin style (optional)

2.1 Beta 2
- fixed site.html
- fixed extension (description as JSON output)
- fix share json
- fix feed class
- remove pwp folder (obsolet!)

2.1 firtz + podlove webplayer 4
- remove search extension and include in firtz (redirect)
- new extension "webplayer" with podlove webplayer version 4 (standrad include)
- fixed opus file and other minimalistics
- create share rendering function in feed.php
- new endpoint for serach requests
- new endpoint to send sharing request
- fixed weblayer css and positions

RC 2.0

1.5 so far:
cleaned structure:
- lib, pwp, js, dict and classes moved to src-folder

changed way templating works:
- main template-folder contains default template (now quorx!)
- additional folders inside template-folder can contain additional files, overriding files inside default folder
- feed.cfg needs template: attribute
- feed.cfg can contain template-vars (go to @templatevars)
- template.cfg inside template-folder can contain default template-vars

1.3 update to podlove webplayer v2.0.13 and support images in mp4chaps

1.2 enabled rfc5005 inside standard feed (until now only by special urls...)
- fixed onother pile of smelly bugs. Take some care though...

1.1 another tons of bugfixes, templates per feed and podlove webplayer 2.0.11
- updated to fatfree 3.0.9, added adnthreads for episode comments

RC 1.0

tons of bugs fixed. podlove webplayer version 2.0.7 integrated

0.13 changed path to pages (now /show/page/@page from /page/@page) and pagers (now /show/pager/@pagenum from /show/page/@pagenum)
- added subdirs for /templates/pages: create dropdowns. only one level
- changed to podlove web player 2.0.5

0.12 fixed bug in markdown parsing (thanks bcosca)
- first (stable? haha) cloning support. call index.php from commandline

0.11 fixed pwp integration bug

0.10 changed to podlove webplayer v2.0.4

0.9 added bitlove support; reintroduced dropdown menus; articles now marked up by markdown

0.8 tons of fixes, typos and stuff. content-extensions.

0.7 autodetect mediafiles with mediabaseurl/path and formats:attribute

0.6 finished first draft of documentation. see doc/firtz.md

0.5 added subtemplate support for head/header/episode/footer
- fixed a bug, in case episodes didn't provide all configured media

0.4 added local auphonic support, yet work in progress
- singlefeed pages redirect to web page on / instead if listing one feed on frontpage

0.3 added first draft of extension class. atm only extends output templates (example: atom-extension. look into ext/atom/)
- changed website URL from /show/$feed to $feed/show to keep consistancy

0.2 major and minor fuckups fixed. thanks to all contributors!

0.1 let the world take a look
