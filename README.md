# Chain Reaction Max — Privacy Policy Site

Developer: **Levi Labs**  
Package: `com.levilabs.chainreactionmax`  
Prepared: 2026-10-27

## CRITICAL: Complete these before publishing

1. **Replace `REPLACE_WITH_YOUR_EMAIL@example.com` everywhere in `index.html` and `delete-account.html`.** Use a real inbox you control that accepts privacy/deletion requests. Remove the coloured placeholder warning at the beginning of each page after replacing it.
2. **Audit and repair account deletion:** Based on a previously shared `settings_screen.dart`, account deletion deletes `users/{uid}`, `currencyTransactions`, `playerNames`, `friendRequests`, `friendships`, `roomInvites`, `currentRooms`, and `presence`, and the Firebase Auth user. It does **not explicitly clean up** every corresponding `rooms`, `onlineMatches` (and `moves` subcollections), or `matchmakingQueue` record. You must assess and delete/anonymise associated data, and handle failures safely. A policy cannot fix backend code.
3. **Verify any enabled features before publication:** Google/Facebook/Google Play Games sign-in methods; guest saving; actual store purchases/ad-free items; available leaderboards; whether Analytics/Crashlytics or other SDKs are included. Remove or revise any wording that doesn't match the production build.
4. **Verify audience and ads:** The draft describes an app not aimed at children under 13. Your Play Console audience selection, screenshots, ads and app behaviour must match. For under-13 target audiences, Google Play Families rules require additional controls.
5. **Implement appropriate ad consent/opt-out:** If showing AdMob personalized ads to the EEA/UK/Switzerland, review Google certified CMP/UMP SDK requirements. Also assess US-state privacy opt-outs where applicable. Simply adding a paragraph in the privacy policy does not implement consent.
6. **Match Play Console Data safety disclosures:** Include Google Mobile Ads automatic collection/sharing of IP (approximate location), user interactions, diagnostics, identifiers, plus Firebase/account/social/game data. Check the current versions actually included in your release.
7. **Add an in-app Privacy Policy link:** Settings (and optionally Login) must open `https://levilabs.github.io/chain-reaction-max-privacy/`. Google Play needs the URL in its Privacy Policy declaration too.
8. **Test deletion request channel:** The external page `https://levilabs.github.io/chain-reaction-max-privacy/delete-account.html` must have a working email link/inbox. Set this as the Play Console **account deletion web URL** when asked.
9. **Verify account security and legal compliance:** Check published Firestore rules, actual cloud-data retention, any required developer contact/address, notices, age-related restrictions, region-specific rights and transfers. Consider qualified legal review for international distribution. No generated policy alone can guarantee compliance with all laws.

## Publish using GitHub Pages

Repository: `https://github.com/LeviLabs/chain-reaction-max-privacy`

1. Edit the two HTML files and replace the email placeholder.
2. Upload `index.html` and `delete-account.html` to the repository **root** (not in a subfolder).
3. In **repository Settings → Pages**, select **Deploy from a branch**, `main`, `/(root)`, Save.
4. When published, open both URLs in an incognito/private window:
   - Privacy Policy: https://levilabs.github.io/chain-reaction-max-privacy/
   - Delete Account: https://levilabs.github.io/chain-reaction-max-privacy/delete-account.html
5. Paste those URLs into the relevant Google Play Console fields.
6. Keep both pages updated whenever the app's real data practices change.

## Google Play requirements (official references)

- User Data policy: https://support.google.com/googleplay/android-developer/answer/10144311
- Data safety form: https://support.google.com/googleplay/android-developer/answer/10787469
- AdMob SDK Data Disclosure: https://developers.google.com/admob/android/privacy/play-data-disclosure
- AdMob Google CMP/consent: https://support.google.com/admob/answer/13554116
- Google Play Families: https://support.google.com/googleplay/android-developer/answer/9893335

**Status:** Comprehensive editable draft; do **not** claim final legal compliance until the requirements above are implemented and verified.
