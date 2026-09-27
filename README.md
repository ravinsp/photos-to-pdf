# Photos to PDF

**This is an AI-generated project**

Live page: https://ravinsp.github.io/photos-to-pdf/

A single-page web app that turns photos into a PDF, with one photo per A4 portrait page. Everything runs in the browser. Photos are never uploaded, and there are no dependencies or build step.

## Running

The app is a single file, `index.html`. Serve it from this folder with Python's built-in web server:

```sh
python -m http.server 8000
```

Then open <http://localhost:8000> in a browser.

To use it from a phone on the same Wi-Fi network, open `http://<your-computer's-IP>:8000` on the phone. The server listens on all network interfaces by default, but your firewall may need to allow port 8000.

Stop the server with `Ctrl+C`.

## Features

- **Select photos**: pick several images at once, and add more later with **＋ Add more**.
- **Sort order**: sort by **Date taken** (read from the JPEG's EXIF data, or the file's modified date if there is none) or by **Selection** order.
- **Per-page controls**: rotate (↻) or remove (✕) any page. Tap a page to preview it full screen.
- **Quality**:

  | Option | Resolution | JPEG quality |
  |---|---|---|
  | Small file | 150 dpi | 70% |
  | Balanced size | 200 dpi | 80% |
  | High quality | 300 dpi | 90% |

- **Layout**: each photo is scaled to fit an A4 page and centred on it. Photos are never enlarged beyond their original resolution.
- **Download**: after **Create PDF**, rename the file if you want, then **Download**.

## Notes

- Formats such as HEIC work only in browsers that can decode them natively (e.g. Safari).
- Changing the photos, their order, rotation or quality discards the PDF you created, and you need to create it again.
