# Photo Location Plan

Builds a site photo location plan from a set of photos. Each photo is pinned at the GPS
location stored in it, with a view cone showing the compass direction the camera faced.
Click a pin to open the photo and its caption.

**Live app:** https://martins3586-ai.github.io/photo-location-plan/

## Features
- Reads GPS position, compass heading and time taken from photo EXIF data (in the browser, nothing is uploaded)
- Numbered pins ordered by time taken, with editable captions
- Place pins or set direction by hand for photos missing that data; drag pins to correct GPS drift
- Base map picker: Satellite (default), Satellite + streets, Street map, or None. Uses Google maps when a Google Maps Platform key works, otherwise the Esri equivalents
- Optional site plan drawing overlay, aligned by drag, resize and rotate
- Google Earth: per-photo "Open in Google Earth" link, and a KMZ export with direction icons and photos in each pin's popup
- Exports: PNG plan with legend, interactive HTML report, Google Earth KMZ, and a JSON project file

## Tips
- iPhone: in the photo picker, check **Options** and make sure location is included.
- Many Android cameras don't record compass direction; set it by hand in the photo view.
- HEIC photos only open in Safari; use JPEG elsewhere.

## Google satellite imagery (optional)
1. In Google Cloud Console, create a project with billing on and enable the **Map Tiles API**.
2. Create an API key. Restrict it to **Websites** `https://martins3586-ai.github.io/*` and to the **Map Tiles API** only.
3. Either paste it into the app (Export menu → *Google imagery key…*; saved in that browser only), or set
   `GOOGLE_MAPS_API_KEY` near the top of the script in `index.html` so every visitor gets Google imagery.

Google's 2D Map Tiles include 100,000 free tile requests per month (then $0.60 per 1,000), with a limit of 15,000 per day.
