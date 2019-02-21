# Proposal: web-font-reducer

## Why?
Many pages embed a whole font file, with all glyphs, for just rendering some headers. This leads to unnecessary downloads for the users, up to 20-40 kb.

## How?
* Scrap the web page with puppeteer to find all usages of the font and then use FontForge to remove all unused glyphs.
* Run a tool in the CI to verify that all wanted glyphs exists in the font files, so that the user don't have to verify each time.
