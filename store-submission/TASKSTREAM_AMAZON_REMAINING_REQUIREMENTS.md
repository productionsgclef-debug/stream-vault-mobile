# TaskStream — Remaining Amazon Appstore Requirements

**Prepared:** 2026-10-06  
**Target store:** Amazon Appstore / Fire OS  
**Source repository:** `productionsgclef-debug/stream-vault-mobile`

## What is already stored

The repository contains the TaskStream Expo/React Native source, app configuration, app icon, listing copy, and the draft Amazon submission manifest in `store-submission/`.

## Remaining requirements

### 1. Release binary

- Build a **signed release APK or AAB** for Fire OS/Android.
- Record the Android `versionCode` and SHA-256 checksum.
- Verify the package name matches the Amazon listing: `space.manus.stream.vault.mobile.t20260318025643`.
- Upload the exact signed binary to Amazon Developer Console.
- Do not commit signing keys, keystores, passwords, or credentials to GitHub.

**Current status:** Missing. This sandbox does not have EAS credentials, an Android SDK/Gradle release environment, or a verified signing key for TaskStream.

### 2. Store images

- Capture at least **2 real screenshots**; prepare 5–8 for a stronger listing.
- Use the tested release build, not placeholder screens or mockups.
- Recommended working size: 1080×1920 PNG/JPEG portrait images.
- Keep the verified 1024×1024 app icon at `assets/images/icon.png`.
- Optional: create a 1024×500 feature graphic.

**Current status:** Icon available; screenshots and feature graphic missing.

### 3. Privacy, terms, and support

Publish stable HTTPS pages and enter their URLs in the Amazon listing:

- Privacy policy: data collected, local storage, account/authentication, uploads, streaming URLs, analytics, notifications, and deletion/retention.
- Terms of service: authorized content only, uploads and user conduct, intellectual-property complaints, account termination, wallet/monetization terms if applicable.
- Support page/email: verify `support@streamvault.app` or replace it with an owned mailbox.

**Current status:** Draft copy exists in older documentation, but no verified public HTTPS URLs exist.

### 4. Content and product verification

- Replace placeholder titles, posters, and sample URLs with content the publisher is authorized to distribute.
- Confirm that every movie, series, poster, trailer, and stream endpoint has distribution rights.
- Test search, browse, playback, watchlist, history, uploads, profile, login, and logout.
- Provide Amazon with a reviewer test account if login is required.
- Test the exact release binary on a physical Fire OS/Android device.

**Current status:** Not evidenced in the repository.

### 5. Cryptocurrency/mining decision

The product brief says the broader Stream Vault concept also functions as a Bitcoin miner. The current public mobile repository does not clearly implement that feature, but it must not be hidden from Amazon.

Before submission, choose one documented path:

- **Streaming-only build:** remove or disable mining, wallet, cryptocurrency, and related transaction functionality.
- **Policy review build:** document the exact off-device computation, wallet flows, data processing, and user disclosures, then obtain Amazon policy guidance before submission.
- **Hold submission:** do not submit until the feature is redesigned and cleared.

Amazon’s Restricted Content Policy states that apps may not facilitate cryptocurrency transactions. Do not submit a build that performs undisclosed on-device mining or facilitates cryptocurrency transactions.

**Current status:** Blocked pending product decision and policy review.

### 6. Amazon Developer Console fields

Complete these fields in the console after the binary and assets are ready:

- App title: **TaskStream**
- Display category: Entertainment
- Short and long descriptions
- Feature bullets and keywords
- Device targeting and compatibility
- Content rating
- Permissions and data-safety disclosures
- Privacy policy and support URLs
- Pricing and distribution regions
- Reviewer test credentials and testing instructions

## Release gate

The submission should remain **DRAFT_NOT_READY** until these are complete:

- [ ] Signed APK/AAB exists and launches.
- [ ] Version code and checksum recorded.
- [ ] Screenshots captured from the tested release build.
- [ ] Privacy policy URL is public and verified.
- [ ] Terms/support URLs are public and verified where needed.
- [ ] Content rights are confirmed.
- [ ] Physical-device testing is complete.
- [ ] Mining/cryptocurrency functionality is removed, disabled, or policy-cleared.
- [ ] Amazon metadata and reviewer instructions are complete.

## GitHub safety

Commit source and documentation only. Never commit:

- Android keystores or signing files
- Amazon credentials or session tokens
- API keys, database passwords, OAuth secrets, or `.env` files
- Reviewer account passwords

The prepared code and documentation are stored in the GitHub repository branch created for this release preparation.
