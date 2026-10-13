Veggie Belgium — MapTiler trilingual FR / NL / EN

READY FOR GITHUB PAGES
======================
Upload all files from this folder to the published GitHub Pages repository, replacing the earlier version (especially index.html). Then refresh the page with Ctrl+F5.

MAP SOURCE
==========
The main road map is MapTiler Streets v4. The MapTiler key supplied for this site is already present in index.html in MAPTILER_API_KEY. It is a browser/public key, not a secret server key. Protect it with an origin whitelist and usage limits in MapTiler Cloud.

MapTiler dashboard > API keys > this key > Allowed HTTP origins:
  antf-web.github.io
If you publish to another hostname, add that hostname too. Leave Allowed User-Agent blank for ordinary browser use. Save the key settings.

Testing with a local file (file://) or localhost can be rejected by an origin-restricted key. Publish to the allowed GitHub Pages host for a conclusive test.

The square map-layer button near the +/- controls lets you switch from MapTiler to CARTO Light or OpenStreetMap. A map-layer fallback also starts automatically if loading fails. Restaurant points are embedded so they do not require Overpass or any external database request.

DATA + TRANSLATIONS
===================
88 OSM restaurant/food venue points are embedded in index.html from restaurants.geojson. Separate data files are supplied for later updates.
English is the fallback language; browser French/Dutch are detected on first visit; visitors may choose EN/NL/FR and the selection is saved.
No customer rating data is supplied in OSM. The site clearly says when ratings are unavailable.

Note: map tile images need internet access, and public tile providers have usage and attribution policies. HTML itself works as a static site.
