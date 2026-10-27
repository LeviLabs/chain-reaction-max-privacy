# Data Safety — assessment worksheet for Chain Reaction Max

This is a starting point, **not** a completed official Data safety declaration. Inspect every release SDK, manifest permission, backend and authentication method before selecting answers in Play Console.

| Data category | Possible details and context | Action before submission |
|---|---|---|
| Personal info | Display name, provider email (if released by provider), cloud Firebase UID, profile photo | Verify Firebase Authentication and enabled Google/Meta providers |
| App activity | Match results, moves, progress, game stats, virtual coins/gems, friends and invites | Confirm which fields leave the device to Firestore |
| Device or other IDs | Google Mobile Ads advertising ID, app-set ID and other IDs | Check SDK and ad ID configuration; include SDK collection |
| Approximate location | AdMob receives IP that can reveal approximate area | Distinguish IP-derived coarse location from precise GPS |
| App interactions | App opens, taps, ads viewed or clicked as available through ads SDK | Check advertising SDK disclosure |
| Diagnostics | Performance, SDK error/hang-related signals | Check SDK disclosure and whether Crashlytics is installed |
| Financial/purchase info | In-app purchase history, entitlements or transaction references only if billing is enabled | Do not assert direct card collection without evidence |
| Sensitive permissions | None can be assumed without inspecting release AndroidManifest | Audit permissions and all SDKs |

## Critical extra sections

- Confirm whether data is **collected**, **shared**, **encrypted in transit**, **optional vs required**, **used for ads / fraud prevention / app functionality / analytics**, and whether deletion can be requested.
- "Shared" means third-party sharing under Google's definition and is affected by the role of service providers and advertising networks. Review the official instructions before marking Yes/No.
- Privacy policy must match Play Console declarations, in-app disclosures, Firebase rules and what the released build actually sends.
- Test external account deletion and in-app deletion of all related records, including matches / room state and subcollections.
- If targeting children, the Families policy adds restrictions beyond this draft.

Official source: https://support.google.com/googleplay/android-developer/answer/10787469
AdMob SDK source: https://developers.google.com/admob/android/privacy/play-data-disclosure
