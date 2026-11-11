# Photo Location Plan

Builds a site photo location plan from a set of photos. Each photo is pinned at the GPS
location stored in it, with a view cone showing the compass direction the camera faced.
Click a pin to open the photo and its caption.

**Live app:** https://martins3586-ai.github.io/photo-location-plan/

## Features
- Reads GPS position, compass heading and time taken from photo EXIF data (in the browser, nothing is uploaded)
- Numbered pins ordered by time taken, with editable captions
- Place pins or set direction by hand for photos missing that data; drag pins to correct GPS drift
- Satellite imagery behind the pins by default (Esri World Imagery), with a toggle to turn it off
- Optional site plan drawing overlay, aligned by drag, resize and rotate
- Google Earth: per-photo "Open in Google Earth" link, and a KMZ export with direction icons and photos in each pin's popup
- Exports: PNG plan with legend, interactive HTML report, Google Earth KMZ, and a JSON project file

## Tips
- iPhone: in the photo picker, check **Options** and make sure location is included.
- Many Android cameras don't record compass direction; set it by hand in the photo view.
- HEIC photos only open in Safari; use JPEG elsewhere.
