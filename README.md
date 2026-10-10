# Carrow Lake Boathouse fixes

1. `hire.html`: the Home link pointed to `index.htm` instead of `index.html`.
2. `hire.html`: the boat photo used an invalid Windows file path, so it never loaded.
3. `index.html`: the Prices link pointed to `prices.html`, but the page is actually in `pages/prices.html`.
4. `index.html`: the ridge photo path was `images/ridge.jpeg`, but the file is actually `images/ridge.jpg`.
5. `pages/prices.html`: the compass photo path was `images/compass.jpg`, but from the `pages` folder it should be `../images/compass.jpg`.
6. In `index.html`, the booking email line was updated to encode the angle brackets as `&lt;` and `&gt;`.
7. The issue that only shows up after upload is the case-sensitive file path problem: `pages/prices.html` used `../images/Logo.svg`, but the actual file is `logo.svg` in lowercase. That works on some Windows machines but fails on Linux web servers because file names are case-sensitive.
