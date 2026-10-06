# TaskStream — Amazon Appstore Submission

**Status: Draft prepared; not submitted**

This folder contains the Amazon Appstore listing manifest for TaskStream. It was prepared from the `stream-vault-mobile` repository at commit `f9bd9e6`.

## Prepared listing

- **Title:** TaskStream
- **Package:** `space.manus.stream.vault.mobile.t20260318025643`
- **Version:** 1.0.0
- **Category:** Entertainment
- **Price:** Free
- **Source repository:** https://github.com/productionsgclef-debug/stream-vault-mobile
- **Reference web app:** https://khaki-stream-task-go.base44.app

The full machine-readable payload is in [`amazon-appstore-submission.json`](./amazon-appstore-submission.json).

## Amazon requirements still outstanding

Amazon’s current submission workflow requires an app binary, app images and descriptions, targeting information, and a physical-device test. The current source does not yet provide all of these items.

| Requirement | Status | Required action |
|---|---:|---|
| Signed Fire OS APK or AAB | **Missing** | Build a release binary with a verified signing key and incremented version code. |
| App icon | Available | Use `assets/images/icon.png`; verify the final dimensions and transparency in the console. |
| Store screenshots | **Missing** | Capture 5–8 real screens from the release build; do not use placeholder artwork. |
| Feature graphic | **Missing** | Create an optional promotional graphic if desired. |
| Privacy policy URL | **Missing** | Publish a policy at a stable HTTPS URL and add it in the app and console. |
| Terms of service URL | **Missing** | Publish terms if the app offers accounts, uploads, monetization, or user-generated content. |
| Support URL/email | Partial | `support@streamvault.app` is listed, but mailbox ownership and a public support page must be verified. |
| Reviewer access | **Missing** | Provide a test account and instructions if login is required. |
| Physical-device test | **Missing** | Test the exact signed build on a compatible Fire OS/Android device. |
| Content rights | **Unverified** | Confirm rights for every movie, series, poster, trailer, and stream URL. |

## Policy blocker requiring a product decision

The TaskStream product brief describes Bitcoin-mining, wallet, monetization, and affiliate functionality. Amazon’s Restricted Content Policy states that apps may not facilitate cryptocurrency transactions. The exact mining implementation is not present in the public `stream-vault-mobile` source inspected for this package, so the listing cannot safely claim or conceal that functionality.

Before submitting, choose and document one of these paths:

1. **Streaming-only release:** remove or disable mining, wallet, and cryptocurrency transaction functionality from the release build and its listing.
2. **Off-device service:** if any mining-related feature remains, document that computation occurs off-device, disclose the data flow, and request Amazon policy guidance before submission.
3. **Do not submit:** keep the release blocked until the feature is redesigned and policy-cleared.

Do not submit an app that mines on the user’s device, hides cryptocurrency functionality, or facilitates cryptocurrency transactions without confirmed policy eligibility.

## Recommended release checklist

- [ ] Resolve the cryptocurrency/mining policy decision.
- [ ] Replace placeholder catalog data and artwork with content that TaskStream is authorized to distribute.
- [ ] Add a public privacy policy and terms/support pages.
- [ ] Build and sign an Android APK or AAB; record the version code and SHA-256 checksum.
- [ ] Test the exact release binary on a physical Fire OS/Android device.
- [ ] Capture store screenshots from the tested build.
- [ ] Complete Amazon content rating, permissions, data-safety, and reviewer-access fields.
- [ ] Review the final metadata and submit manually from the Amazon Developer Console only after all blockers are cleared.

## Submission boundary

This package intentionally does **not** submit anything to Amazon. Publishing an app creates an external developer-console record and sends the app for review; it should happen only after the missing binary, assets, rights, privacy URL, and cryptocurrency-policy decision are resolved and the final payload is reviewed.
