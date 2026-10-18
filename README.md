# Hospital Phrases

A lightweight, large-button web app for hospital visits. A family member or caregiver records short phrases in their own language (for example Teochew, Mandarin, or Khmer). The patient or staff can then tap any phrase to hear it in English or in the recorded voice.

Works on phones, foldables, and tablets. Installable, and usable offline after the first visit.

## Use it

- **Use mode:** tap **English** or **Native** on any card to play it. Yes, No, and "Are you in pain?" are pinned at the top. Other phrases are in the Basics, Pain & Symptoms, and Needs tabs.
- **Setup mode** (for the caregiver):
  - Tap **Record**, speak, then tap **Stop** (it also stops by itself after 10 seconds).
  - Use **Re-record** to replace a recording.
  - **Add phrase** adds your own phrase to the current tab. Custom phrases can be deleted.
  - **Export all** saves one `.json` file with all recordings and custom phrases. Share it or keep it as a backup.
  - **Import file** loads an export. If items already exist, choose **Replace** or **Fill in missing**.

## Privacy

Recordings are stored only in the browser on the device (IndexedDB). Nothing is uploaded unless you share an export file yourself. Clearing browser data erases recordings, so export a backup now and then.

## Deploy on GitHub Pages

1. Create a public repository.
2. Upload all files in the repo root: `index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, and this README.
3. Go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. Your app is at `https://YOUR-USERNAME.github.io/REPO-NAME/` after a minute or two.

To publish an update, replace the files and change the cache name in `sw.js` (for example `phrases-v2` to `phrases-v3`).

## Install and offline

Open the link once while online.
- **Android (Chrome):** menu, then **Install app**.
- **iPhone (Safari):** Share, then **Add to Home Screen**.

## Notes

- Recording needs HTTPS (GitHub Pages provides it) and microphone permission. If it is blocked, a button offers the phone's own recorder app instead.
- English audio uses the device's built-in voice, so it sounds different on different devices.
- Recordings made on Android (WebM) may not play on iPhones, and the reverse. For sharing between platforms, record on the same type of device.
- Browser storage is shared across everything on `username.github.io`, so this app uses its own namespaced keys.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (HTML, CSS, JavaScript) |
| `sw.js` | Service worker for offline use |
| `manifest.webmanifest` | Install settings |
| `icon-192.png`, `icon-512.png` | App icons |
