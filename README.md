# MusicBox Phone (offline app for Android)

A web app you install on your home screen. After the first setup it works with no internet. It only keeps the songs you choose.

## Step 1: Put the app online once (free)

An installable app must be loaded from an https address one time. The free way is GitHub Pages.

1. Go to github.com and make a free account (or log in).
2. Tap **+** → **New repository**. Name it `musicbox`, set it to **Public**, and create it.
3. Click **uploading an existing file**. Upload all 5 files from this folder:
   `index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`.
   Click **Commit changes**.
4. Go to the repository **Settings → Pages**. Under "Branch" choose `main` and `/ (root)`, then **Save**.
5. Wait 1–2 minutes. Your address will be: `https://YOURUSERNAME.github.io/musicbox/`

Only the app files go online. Your songs never leave your phone.

## Step 2: Install it on your Poco X2

1. Open that address in **Chrome** on the phone.
2. Chrome menu (⋮) → **Install app** (or **Add to Home screen**).
3. Open MusicBox from the new home-screen icon.
4. Turn on airplane mode and open it again to check that it works offline.

## Step 3: Get songs onto the phone

1. Copy the songs you want from your laptop to the phone with a USB cable (for example into the `Music` folder).
2. In MusicBox tap **+ Add songs** and select them. Select many at once if you like.
3. MusicBox keeps its own copy inside the app, so the app uses extra storage equal to the size of those songs. The top of the screen shows how much it is using. After adding, you can delete the originals from the phone if you want the space back.
4. It reads the title, artist and cover picture from the file when they exist. Use ⋮ on a song to rename it, set the artist, or set a cover picture.

## Keep music playing with the screen off (Xiaomi / Poco)

Xiaomi's battery saver often kills background music. Do this once:
- **Settings → Apps → Manage apps → MusicBox** (or Chrome) → **Battery saver → No restrictions**.
- Also turn on **Autostart** for it, and lock it in the recent-apps screen (pull down on its card, tap the lock).

## Updating later

If you replace `index.html` on GitHub, edit `sw.js` and change `musicbox-v1` to `musicbox-v2` so phones download the new version.

## Known limitations

- Not tested on a real phone; only the code was syntax-checked and the tag reader was tested with sample data. Expect to send me any bugs you find.
- Android can clear the app's stored songs if the phone is almost out of storage or you clear Chrome's site data. MusicBox asks Android to protect them, but it can't promise that. Keep your originals as a backup.
- Add songs one batch at a time on slow phones; large batches can take a while.
- The artist is blank when the file has no tag. Set it from the ⋮ menu.
- The page's colours come from each cover picture; songs without a cover use the plain dark background.
- It can't read your laptop's `library.json`; the phone has its own separate library.
