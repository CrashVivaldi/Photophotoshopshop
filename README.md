# Photophotoshopshop

Browser-based image tools — no install, no AI, no server round-trip.

Open `index.html` in a browser (or serve the folder with any static file server).

## Tools

### Color Layer Split (`layer-split.html`)

Photo of a drawing in → layered PSD out, one layer per distinct color.

Pipeline: load image → Wu quantizer with CIE94 color distance (`image-q`) → paper/background detection → per-color transparent masks → PSD export (`ag-psd`). Everything runs client-side.

**Tips for best results:** flat, square-on photo with even lighting. Crop or straighten before uploading if the page isn't aligned.
