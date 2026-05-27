# Privacy Policy — Volume Booster Pro

**Last updated:** 27 May 2026
**Developer:** Suraj Subedi ([subedisuraj.com.np](https://subedisuraj.com.np))
**Contact:** soorajsubedi1227@gmail.com

Volume Booster Pro is a Chrome extension that amplifies and equalizes audio on browser tabs. This document explains, in plain language, exactly what data the extension touches and what it does *not* touch.

---

## Short version

Volume Booster Pro **does not collect, transmit, sell, or share any personal data**. Everything you configure stays on your own computer, in Chrome's local extension storage. The extension makes no network requests of its own.

---

## 1. What data is stored

The extension uses `chrome.storage.local` — a browser-managed key-value store that lives on your device — to remember your preferences between sessions. The following items, and only the following items, are stored:

| Key | Contents |
|---|---|
| `siteVolumes` | Map of domain → volume percent (e.g. `youtube.com → 80`) |
| `siteEQ` | Map of domain → equalizer bands `{ bass, mid, treble }` in dB |
| `presets` | Your built-in and custom volume presets (name, icon, volume) |
| `settings` | Mute-fade toggle and fade duration |
| `theme` | Selected color theme (e.g. `"ocean"`) |

These keys are written and read by the extension on your machine only. They are never copied off your device, never uploaded to a server, never associated with an account, and never shared with the developer or any third party.

You can inspect or wipe this data at any time:
- **In the extension:** open the popup → Settings (gear icon) → *Clear saved site volumes* or *Reset all settings*.
- **In Chrome:** uninstall the extension. All `chrome.storage.local` data for it is deleted automatically.

---

## 2. What data is *not* collected

To be explicit, Volume Booster Pro does **not** collect, log, transmit, or have access to any of the following:

- Your name, email address, phone number, or any account information
- Your browsing history or list of visited URLs
- Page content (text, images, video, audio)
- Cookies, login credentials, or authentication tokens
- IP address, geolocation, or device identifiers
- Click streams, keystrokes, mouse movements, or any analytics
- Health, financial, or any other personally identifiable information

The extension does **not** include Google Analytics, Sentry, Mixpanel, or any other third-party SDK, telemetry endpoint, or tracking pixel.

---

## 3. Network activity

Volume Booster Pro **does not make any outbound network requests** during normal operation. There is no backend server, no API call, no analytics ping, no auto-update endpoint beyond Chrome's standard extension delivery.

The only situations where a network request happens are user-initiated and use the browser's own facilities, not the extension's:

- Clicking the **Buy me a coffee** link opens `buymeacoffee.com/volume_booster_pro` in a new tab.
- Clicking the **website** icon opens `subedisuraj.com.np` in a new tab.
- Clicking **Request a feature → Open mail app** opens your system's default mail client with a `mailto:` link addressed to `soorajsubedi1227@gmail.com`. The extension itself does not send the message — your mail client does.
- Clicking a **Quick Access** button (YouTube / Spotify / Netflix) opens the relevant site in a new tab if no matching tab is already open.

In every case the request originates from your browser, not from the extension's code, and is governed by Chrome's normal network and privacy rules.

---

## 4. Permissions and why they exist

The extension declares the following Chrome permissions. None of them are used to collect data.

| Permission | Used for |
|---|---|
| `activeTab` | Apply volume/mute/EQ to the tab you're currently viewing |
| `tabs` | List tabs that are currently playing audio in the popup |
| `contextMenus` | Add right-click entries (Mute, Set Volume) |
| `storage` | Save your preferences locally on your own device |
| `scripting` | Inject the audio controller into tabs that were open before the extension was installed |
| `<all_urls>` host permission | Connect to `<audio>` and `<video>` elements on whatever sites you choose to play media on |

Host access (`<all_urls>`) is broad because audio boosting is a site-agnostic feature — there is no way to know in advance which sites you will play audio on. The content script only ever reads and modifies media elements; it never reads page text, form input, cookies, or storage.

---

## 5. Children's privacy

Volume Booster Pro is a general-purpose audio utility. It does not knowingly target children under 13, does not collect any data from anyone, and stores no personal information of any kind. There is no account system and no way for the developer to learn the identity or age of any user.

---

## 6. Third parties

Volume Booster Pro has no third-party data processors. The brand logos shown in the Quick Access bar (YouTube, Spotify, Netflix) are static SVG icons bundled into the extension; the extension does not interact with those companies' APIs and does not share any information with them.

---

## 7. Changes to this policy

If this policy ever changes — for example, if a future version adds a backend feature that involves network activity — the change will be reflected here, and the version will be noted at the top of this document. Continued use of the extension after a policy change implies acceptance of the updated policy.

---

## 8. Contact

Questions, concerns, or data-deletion requests:

- **Email:** soorajsubedi1227@gmail.com
- **Website:** [subedisuraj.com.np](https://subedisuraj.com.np)
- **In-app:** open the popup, click the message-bubble icon in the header, send a feature request or report.

Because no data ever leaves your machine, there is nothing for the developer to delete on your behalf — uninstalling the extension or using the *Reset all settings* button removes everything.
