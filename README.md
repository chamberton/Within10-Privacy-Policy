# Within 10 — Privacy Policy

**Last updated:** 7 October 2026  
**Applies to:** Within 10 (also shown as “Within X” in some screens) on iOS and Android  
**Developer:** Serge Mbamba  

This document describes how the Within 10 mobile application (“**App**”, “**we**”, “**us**”) handles information when you use it. By using the App, you agree to this policy. If you do not agree, please do not use the App.

**Canonical URL:** [https://within10.app/privacy](https://within10.app/privacy) (may point to this repository).  
**In-app link:** Settings → Privacy policy (loads this policy from the web).

---

## Summary

- We use your **location** to find places near you and, if you enable it, to alert you when you are close to saved places.
- We **do not sell** your personal data and **do not show third-party advertising** in the App.
- **Place search** is powered by **Google Places**; requests go to Google under [Google’s terms and privacy policies](https://policies.google.com/privacy).
- **Subscriptions** are processed by **Apple App Store** or **Google Play**; we do not receive your full payment card details.
- Most saved data (favourites, cache, settings) stays **on your device** unless you use features that sync a limited trial record to our backend.

---

## 1. Information we collect and use

### 1.1 Location

When you grant permission, the App uses your device’s location to:

- Search for restaurants, hotels, bars, cafés, and other places within the radius you choose;
- Show distance and “open now” information;
- Optionally run **proximity alerts** for places you have saved (including background location if you allow it).

Location is used for these features only. We do not use location to build advertising profiles. You can revoke location access in your device settings at any time; some features will not work without it.

You may also search around a **manually chosen** location (via place autocomplete). That choice is used for search until you switch back to GPS.

### 1.2 Data stored on your device

The App stores data locally on your phone or tablet, including:

- **Saved places and collections** (favourites);
- **Cached place details** (names, ratings, photos metadata, opening hours, etc.) to speed up browsing and support offline access for saved content (Within X Pro / Pro Max);
- **App settings** (language, enabled place categories, search radius, theme);
- **Trial and entitlement state** (start time, last seen, platform) in local storage;
- **Meeting-related content** you choose to protect (may use device biometrics / secure storage);
- **Invitation contacts** you add for meeting invitations (stored locally unless you export or share them yourself).

You can clear cached data from Settings where the App provides that option.

### 1.3 Account and trial sync (Firebase)

To enforce a **free trial** and sync trial timing across reinstalls when online, the App may:

- Sign you in with **Firebase Anonymous Authentication** (a random user ID, not your name or email);
- Write a **trial record** to **Google Cloud Firestore** containing:
  - A **one-way hash** of a device identifier (the raw identifier is not sent to our servers);
  - Trial start time and last-seen time;
  - Platform (`ios` or `android`);
  - Schema version;
  - The anonymous Firebase user ID (for access control only).

We do **not** use this to track your real-world movements or to sell data. If sync fails (offline or error), the App falls back to locally stored trial data.

Legacy Firestore collections used by older App versions are **denied** by current security rules and are not written by current releases.

### 1.4 Analytics and diagnostics

We use **Firebase Analytics** for aggregated usage events (for example, place category searches and some feature usage). We use **Firebase Crashlytics** to collect crash logs and technical diagnostics to fix bugs. These services are provided by Google; they may receive device and app version information as described in [Google’s privacy documentation](https://firebase.google.com/support/privacy).

We configure crash reporting to be **disabled in debug builds** where applicable. We avoid logging API keys or precise location in crash reports.

### 1.5 Contacts

If you use **save to contacts** or **meeting invitations**, the App may access your address book **only when you initiate that action**. Contact data you select is used to create or update contacts on your device or to compose invitations; we do not upload your full address book to our servers.

### 1.6 Photos

If you save images to your photo library, the App requests photo library permission for that action only.

### 1.7 Purchases

**Within X Pro** and **Within X Pro Max** subscriptions are sold through the **Apple App Store** or **Google Play**. Payment is handled entirely by Apple or Google. We receive purchase tokens / subscription status needed to unlock paid features, not your full payment credentials.

Apple’s terms: [https://www.apple.com/legal/internet-services/itunes/dev/stdeula/](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/)

### 1.8 Google Places and maps

Place search, details, photos, and autocomplete are requested from **Google Places API** (and related Google services). Those requests include search parameters and location coordinates needed to return results. Google processes this data under its own policies: [https://policies.google.com/privacy](https://policies.google.com/privacy).

When you tap **Navigate**, **Call**, or **Website**, the App opens your device’s maps, phone, or browser apps; those services have their own privacy terms.

### 1.9 Export

If you use **export data** (paid feature), the App generates a file from data stored on your device and shares it through the system share sheet. We do not receive a copy unless you send it to us yourself.

---

## 2. What we do not do

- We **do not sell** your personal information.
- We **do not display third-party advertising** in the current App (no ad network monetization).
- We **do not require** a named account, email, or password to use the core App (anonymous auth is used only for trial sync).

---

## 3. Legal bases (EEA / UK)

Where GDPR or UK GDPR applies, we rely on:

- **Contract / steps at your request:** providing search, favourites, subscriptions, and features you activate;
- **Legitimate interests:** security, fraud prevention for trials, analytics and crash fixing in proportion to impact;
- **Consent:** where required for optional permissions (location, contacts, photos, notifications, background location).

You may withdraw consent for permissions in device settings; withdrawal does not affect processing already performed.

---

## 4. Retention

- **On-device data** remains until you delete it, clear cache, or uninstall the App.
- **Firestore trial records** are kept as long as needed to operate the trial and subscription model; you may contact us to request deletion where applicable law gives you that right.
- **Analytics and crash data** are retained according to Google Firebase default retention settings; we use them only for product improvement.

---

## 5. Sharing and processors

We share information only with:

| Recipient | Purpose |
|-----------|---------|
| **Google** (Places API, Firebase Auth, Firestore, Analytics, Crashlytics) | Place data, authentication, trial sync, analytics, crashes |
| **Apple / Google** | In-app purchases and subscription validation |
| **Service providers** | Hosting and infrastructure strictly necessary to operate Firebase |

We do not authorize these providers to use your data for their own marketing unrelated to providing services to us.

---

## 6. International transfers

Firebase and Google services may process data in the United States and other countries. Where required, we rely on appropriate safeguards (such as standard contractual clauses offered by Google for Firebase).

---

## 7. Security

We use industry-standard measures including encrypted transport (HTTPS), Firestore security rules, hashed device identifiers for trial documents, and platform secure storage where available. No method of transmission or storage is 100% secure.

---

## 8. Children

The App is not directed at children under 13 (or the minimum age in your country). We do not knowingly collect personal information from children. If you believe a child has provided us data, contact us and we will take appropriate steps to delete it.

---

## 9. Your rights

Depending on where you live, you may have rights to **access**, **correct**, **delete**, **restrict**, **object**, or **port** personal data, and to **complain** to a supervisory authority.

To exercise rights or ask questions, contact us (Section 11). For purchases, subscription management, and refunds, use **App Store** or **Google Play** account settings as well.

---

## 10. Changes

We may update this policy when the App or legal requirements change. We will post the new version in this repository and update the “Last updated” date. Continued use after changes means you accept the updated policy.

---

## 11. Contact

**Privacy questions and requests:**

- Open an issue: [github.com/chamberton/Within10-Privacy-Policy/issues](https://github.com/chamberton/Within10-Privacy-Policy/issues)

Please include your platform (iOS/Android), App version (Settings → About), and a clear description of your request.

---

## 12. App Store disclosure (short form)

**Within 10** uses location to find nearby places and optional proximity alerts; contacts access only when you save or invite; local storage for favourites and cache; Google Places for search; Firebase for anonymous trial sync, analytics, and crash reports; Apple/Google for subscriptions. No sale of personal data. No in-app ads.
