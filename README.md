# ELVOAQ — direct downloads

Installers for the **ELVOAQ Vault** apps, for people who want them without
going through Google Play or the App Store. There is no source code here; this
repository exists only to host release files.

**Everything is on the [Releases page](https://github.com/ELVOAQOFFICIAL/elvoaq-downloads/releases/latest).**

| File | Platform | What it is |
|---|---|---|
| `ELVOAQ-<version>.apk` | Android 8.0+ | The finished app, signed by ELVOAQ. Install it directly. |
| `ELVOAQ-<version>-sideload.ipa` | iPhone / iPad, iOS 26+ | An **unsigned** build. You sign it yourself with your own Apple ID using AltStore, SideStore or Sideloadly. |

Both connect to the same ELVOAQ account as the web app at
[elvoaq.com](https://elvoaq.com). Nothing here is a different or cut-down
version — it is the same build, delivered a different way.

---

## Android

1. Open the [latest release](https://github.com/ELVOAQOFFICIAL/elvoaq-downloads/releases/latest)
   on your phone and download the `.apk`.
2. Tap it. Android will say the file came from an unknown source — choose
   **Settings**, allow installs from your browser, then go back and tap
   **Install**.
3. That is it. Updates are not automatic: come back here for a newer release.

**Check you got the real file.** Every release lists the APK's SHA-256 and the
signing certificate fingerprint. The certificate never changes, so an update
that refuses to install over your existing copy was not signed by us:

```
SHA-256: E9:5F:6B:39:39:A1:60:CE:24:ED:C6:1F:6E:51:0C:BC:42:53:A6:78:0A:C6:26:B7:0C:A2:A0:2D:95:17:5A:F8
SHA-1:   F1:CF:26:93:C8:2B:E1:39:DD:1F:BA:15:95:14:27:10:4E:D1:C5:B8
```

You can verify it yourself with `apksigner verify --print-certs ELVOAQ-<version>.apk`.

---

## iPhone and iPad

Apple does not allow an app to be installed from a website, so the `.ipa` here
is **unsigned on purpose**: you sign it with your own Apple ID, which is the
only route Apple permits outside the App Store. You need a computer once, to
do the signing.

**Pick one tool:**

- **[AltStore](https://altstore.io)** or **[SideStore](https://sidestore.io)** —
  installs the app and can refresh it for you in the background.
- **[Sideloadly](https://sideloadly.io)** — simplest one-off install; Windows or Mac.

**Then:**

1. Install the tool on your computer and follow its own first-time setup.
2. Download `ELVOAQ-<version>-sideload.ipa` from the
   [latest release](https://github.com/ELVOAQOFFICIAL/elvoaq-downloads/releases/latest).
3. Connect your iPhone, point the tool at the `.ipa`, and sign in with your
   Apple ID when asked. Use an Apple ID you are willing to sign apps with.
4. On the iPhone, open **Settings → General → VPN & Device Management** and
   trust the developer profile that appears. The app will not open until you do.

**What to expect, honestly:**

- **A free Apple ID expires the app after 7 days.** Re-sign it with the same
  tool to keep going. AltStore and SideStore can do this automatically while
  your phone is on the same network as your computer. A paid Apple Developer
  account (99 USD/year) extends it to a year.
- **Push notifications, Sign in with Apple and password autofill will not
  work.** Those need entitlements only ELVOAQ's own signature carries, and
  re-signing strips them. Sign in with an email and password, or with Google.
- Everything else — your vault, photos, sharing, the AI assistant, purchases
  made on the web — works normally.
- A free Apple ID can hold **three** sideloaded apps at a time.

If none of that appeals, the App Store version is the easier path once it is
available.

---

## Which is newer?

Releases are tagged with the app version and build, e.g. `v1.0-46`. The
version shown in the app under **Settings → About** matches the tag.

## Problems

Email **support@elvoaq.com** with the release tag and what happened.
Please do not open issues here — this repository holds files, not code.
