# DE ESPACIO Wi-Fi Voucher Generator

A static browser app for generating DE ESPACIO voucher artwork using the supplied `Template-06.png` background. It supports QR generation, editable voucher details, batch generation, individual PNG downloads, and browser print / Save as PDF.

## Deploy to GitHub Pages

1. Create a new public repository named `de-espacio-voucher-generator` in your GitHub account (`ishall21`).
2. Upload `index.html`, `README.md`, and the `assets/` folder. Keep the file paths unchanged.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then save.
6. Wait for GitHub Pages to publish. The site URL will usually be `https://ishall21.github.io/de-espacio-voucher-generator/`.

## Use

- Set the portal URL (default: `http://deespacio.net`).
- Choose username prefix, starting number, password mode, batch quantity, profile, download rate, and shared users.
- Click **Generate voucher(s)**.
- Download individual PNG files or use **Print / Save PDF**.

## Important notes

- This is a static frontend. It does **not** create users on MikroTik or integrate with a billing platform.
- QR mode `Portal URL only` is the safest default and simply encodes the configured portal URL.
- QR mode `Portal URL + username` adds the username as a `username` query parameter; your login page must support that parameter for autofill. It does not include the password in the URL.
- QR mode `Show username and password as text` encodes the credentials in the QR payload. Anyone scanning it can read those credentials; use only when intended.
- The page loads QRCode.js from a CDN, so an internet connection is needed for QR generation.
- Avoid putting real customer credentials in a public repository. The app itself does not upload generated vouchers, but the deployed page is publicly accessible.
