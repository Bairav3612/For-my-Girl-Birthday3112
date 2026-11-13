# Boomika's Purple Galaxy Birthday Surprise

A responsive birthday website with six clickable 3D-flip photo symbols, background music, a personal voice message, falling petals, 100 birthday reasons, a letter, a secret gift and a countdown.

## Project files

- `index.html` — website structure
- `style.css` — purple galaxy design and flip-card animations
- `script.js` — photo cards, music, voice, reasons, gift and countdown
- `assets/photos/` — add six photos named `photo1.jpg` through `photo6.jpg`
- `assets/audio/` — add `background.mp3` and `voice-message.mp3`

## Add your six photos

Copy your images into `assets/photos/` and use these exact filenames:

1. `photo1.jpg`
2. `photo2.jpg`
3. `photo3.jpg`
4. `photo4.jpg`
5. `photo5.jpg`
6. `photo6.jpg`

Click a symbol on the website to flip the card and reveal its photo inside the same card. Click it again to hide the photo.

## Add background music

Put a music file you own or are licensed to use at:

`assets/audio/background.mp3`

The visitor must click **Music: off** to start playback. Browsers block automatic audio playback until a user interacts with the page.

## Add your voice recording

Record your birthday message and save it as an MP3 file here:

`assets/audio/voice-message.mp3`

The voice player is in the “A message, in my voice” section. Background music pauses while the voice note is playing.

## Run on Windows 11

1. Extract the project ZIP.
2. Open the extracted project folder in File Explorer.
3. Click the address bar, type `cmd`, and press Enter.
4. Run:

   ```bash
   py -m http.server 8000
   ```

5. Open `http://localhost:8000` in your browser.
6. Keep the terminal window open while using the site. Press `Ctrl+C` to stop the server.

If `py` is unavailable, try `python -m http.server 8000`.

## Run on Kali Linux

Open a terminal in the project folder and run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in Firefox or Chromium. Press `Ctrl+C` to stop the server.

## Countdown date

The countdown is set to 31 December 2026 at midnight in the visitor's local timezone. To change it, edit this line in `script.js`:

```js
const birthday = new Date(2026, 11, 31, 0, 0, 0).getTime();
```

JavaScript months are zero-indexed: December is `11`.

## Publish online

Upload `index.html`, `style.css`, `script.js`, `README.md`, and the complete `assets` folder to a GitHub repository, then enable GitHub Pages under **Settings → Pages**. You can also deploy the extracted folder using Netlify Drop.

Only publish photos and recordings you have permission to share. Anyone with access to a public website link may be able to view its contents.
