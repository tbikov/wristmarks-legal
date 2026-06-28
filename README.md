# WristMarks — Legal

Public hosting for the WristMarks iOS app's **Privacy Policy**.

- **Live URL:** https://tbikov.github.io/wristmarks-legal/ (GitHub Pages, source: `main` / root)
- **In-app link:** Settings → Privacy Policy (points to the URL above)
- **App Store Connect:** paste the same URL into the app's Privacy Policy URL field
- **Contact:** tsvyatkobikov@gmail.com

## ⚠️ Keep the policy in sync with the app

Whenever a feature changes **what data the app handles or where it goes**, update `index.html` here and commit (GitHub Pages redeploys automatically). Update the **Effective** date when you do.

What to add, and where in the policy, for common changes:

| Change in the app | What to add to the policy |
|---|---|
| **AI photo recognition (V2)** — sends a watch photo to the developer's Azure Function → Anthropic (Claude) | A new "AI Watch Recognition" section: photo + chosen specs leave the device, sent to the proxy and to Anthropic for analysis, **not used for model training**, retention details. (BYO-API-key mode: state the photo goes directly to the user's chosen provider under that provider's policy.) |
| **Any analytics / crash reporting SDK** | A "Analytics" section naming the SDK + what it collects; and flip the App Store "App Privacy" label to match (Apple auto-rejects mismatches). |
| **Accounts / login / cloud backend** | A section on what account data is stored and where. |
| **New third-party network service** (beyond Open-Meteo, OpenStreetMap, Apple iCloud) | Add it to the "Third-party services" list with a link to its policy. |
| **New on-device permission** (e.g. Camera, Contacts) | State what it's used for and that data stays on-device unless otherwise noted. |
| **Purchases / subscriptions** | Note that purchases are handled by Apple; the developer doesn't receive payment details. |

Rule of thumb: if a change makes data **leave the device** or adds a **third party**, it must be reflected here *before* that version ships.
