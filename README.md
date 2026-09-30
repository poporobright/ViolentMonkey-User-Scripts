# Userscripts

A collection of userscripts for [Violentmonkey](https://violentmonkey.github.io/). Each script is a single `.user.js` file you can install in a few clicks.

## Scripts

| Script | Description | Install |
| --- | --- | --- |
| **Web EQ** | 10-band equalizer with preamp, presets and limiter. Adds an EQ button next to the YouTube search bar and in the player controls. Works on YouTube, YouTube Music, Vimeo, Twitch, Dailymotion and SoundCloud. | [Install](https://github.com/poporobright/ViolentMonkey-User-Scripts/releases/download/Files/web-eq.user.js) |

> Replace `YOUR_USERNAME/YOUR_REPO` with your GitHub username and repository name, and adjust the branch name if it isn't `main`.

---

## Requirements

A userscript manager. These scripts are written and tested for **Violentmonkey**, available for Chrome, Edge, Firefox, and other Chromium-based browsers. Get it from [violentmonkey.github.io](https://violentmonkey.github.io/get-it/).

---

## Installation

Pick whichever method is easiest for you.

### Method 1: One-click install (recommended)

1. Install Violentmonkey (see above).
2. Click the **Install** link for the script in the table above (or open the script's `.user.js` file in this repo and click the **Raw** button).
3. Violentmonkey opens an install page showing the script's details.
4. Click **Install** (or **Confirm installation**).
5. Visit a supported site and reload the page.

### Method 2: Download the file

1. Click the `.user.js` file in this repo.
2. Click the **Download raw file** button (the download icon at the top right of the code view), or right-click **Raw** and choose **Save Link As...**.
3. Make sure the file name still ends in `.user.js`.
4. Drag the file into a browser window. Violentmonkey shows the install page. Click **Install**.

> **Chrome/Edge:** dragging a local file requires enabling **Allow access to file URLs** for Violentmonkey on the `chrome://extensions` (or `edge://extensions`) page. If you'd rather not, use Method 3.

### Method 3: Copy and paste

1. Open the script's `.user.js` file in this repo and click the **Copy raw file** button.
2. Click the Violentmonkey icon in your toolbar, then click **+** and choose **New**.
3. Select everything in the editor, delete it, and paste the script.
4. Press **Cmd+S** (macOS) or **Ctrl+S** (Windows/Linux) to save.

---

## Verify it works

1. Open the **Violentmonkey dashboard** (toolbar icon, then the gear/dashboard icon). The script should appear in the list with the toggle switched on.
2. Go to a site the script supports and reload the page.
3. Click anywhere on the page once. Browsers require a click before audio can be processed.

For **Web EQ** on YouTube, look for the EQ icon to the left of your profile picture (next to the search bar) and in the bottom-right of the video player controls.

---

## Updating

- Re-install the script using any method above. Violentmonkey will offer to update it.
- If a script's header includes `@updateURL` and `@downloadURL`, Violentmonkey can update it automatically. You can also click **Check for updates** in the dashboard.

---

## Adding more sites

Each script has a metadata block at the top of the file. To enable a script on another site, add a `@match` line:

```js
// @match        https://www.example.com/*
```

Open the script in the Violentmonkey dashboard, edit the header, and save. Some sites (Netflix, Spotify Web, other DRM-protected or cross-origin media) block the Web Audio API, so Web EQ will not work there.

---

## Troubleshooting

**The script doesn't appear to run**
- Confirm it's enabled in the Violentmonkey dashboard and that Violentmonkey itself is enabled for the site.
- Reload the page after installing.
- In Chrome/Edge, check the extension's details page for a **Developer mode** or **Allow User Scripts** toggle. Newer browser versions may require it before any userscript manager can run scripts.

**No EQ button on YouTube**
- Click once on the page, then wait a second or two. Buttons are added after YouTube finishes loading its interface.
- YouTube changes its page layout from time to time. If the buttons disappear after a YouTube update, please open an issue.

**No sound or no effect on a site**
- The site may serve audio in a way the Web Audio API can't process (DRM or cross-origin). Remove that site from the `@match` list.

**Settings don't carry over between sites**
- Settings are stored per site (for example, youtube.com and music.youtube.com are separate).

---

## Security

Userscripts run with access to the pages you visit. Before installing any script, including these, open it and read through the code. Only install scripts from sources you trust.

## Contributing

Bug reports and suggestions are welcome. Open an issue and include your browser, your Violentmonkey version, and the site where the problem occurs.

## License

MIT License.
