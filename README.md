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
- **Subscriptions** are processed by **Apple App Store** (iOS) or **Google Play** (Android); we do not receive your full payment card details.
- On **iPhone and iPad**, **Apple** provides the store, payment, and many system permissions; see [§ Apple privacy and services (iOS)](#apple-privacy-and-services-ios).
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

**Within X Pro** and **Within X Pro Max** subscriptions are sold through the **Apple App Store** (iOS) or **Google Play** (Android). Payment is handled entirely by Apple or Google. We receive purchase tokens / subscription status needed to unlock paid features, not your full payment credentials.

**On iOS**, your subscription is tied to your **Apple ID**. Manage or cancel it in **Settings → [your name] → Subscriptions**. Refunds and billing disputes for App Store purchases are handled by Apple under its policies, not by us directly.

- Apple Standard Licensed Application EULA: [https://www.apple.com/legal/internet-services/itunes/dev/stdeula/](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/)
- Apple Media Services Terms: [https://www.apple.com/legal/internet-services/itunes/](https://www.apple.com/legal/internet-services/itunes/)

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
| **Apple** (App Store, StoreKit, iOS) | Distribution, subscription billing, subscription status; platform permission UI; on-device biometrics for optional meeting lock |
| **Google Play** | Android distribution, subscription billing, subscription status |
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

To exercise rights or ask questions, contact us (Section 12). For **iOS** billing, refunds, and subscription management, use **Apple** (Section 10). For **Android**, use **Google Play**.

---

## 10. Apple privacy and services (iOS)

Within 10 is **deployed on iOS** through the [Apple App Store](https://apps.apple.com/). When you use the App on iPhone or iPad, you also interact with **Apple’s platform and services**, which have privacy practices **separate from this policy and from Serge Mbamba (the developer)**.

### 10.1 What Apple provides

- **App distribution and updates** via the App Store.
- **In-app purchases and auto-renewable subscriptions** via **StoreKit**; Apple processes payment and maintains your subscription relationship with your Apple ID.
- **System permission dialogs** for location (including background location if you allow it), contacts, photos, notifications, and **Face ID / Touch ID** when you use optional meeting protection. Biometric data is handled **on your device by iOS**; we do not receive your fingerprint or face data.
- **Optional App Tracking Transparency (ATT)** prompts on some iOS versions if the App requests tracking authorization. We **do not sell your data** and **do not show third-party ads** in the App; you may decline tracking if prompted without losing core place search features.

### 10.2 Apple privacy and legal documents

Read Apple’s own policies for how Apple uses information when you use the App Store, your Apple ID, and iOS:

| Topic | Link |
|-------|------|
| Apple Privacy Policy | [https://www.apple.com/legal/privacy/](https://www.apple.com/legal/privacy/) |
| Apple Privacy (overview) | [https://www.apple.com/privacy/](https://www.apple.com/privacy/) |
| Control your Apple privacy choices | [https://www.apple.com/privacy/choices/](https://www.apple.com/privacy/choices/) |
| Apple Media Services Terms | [https://www.apple.com/legal/internet-services/itunes/](https://www.apple.com/legal/internet-services/itunes/) |
| Standard Licensed Application EULA | [https://www.apple.com/legal/internet-services/itunes/dev/stdeula/](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/) |
| Privacy — App Store & Apple media apps | [https://www.apple.com/legal/privacy/data/en/app-store/](https://www.apple.com/legal/privacy/data/en/app-store/) |

### 10.3 App Store “App Privacy” label

Apple requires a **Privacy Nutrition Label** on our App Store product page. It lists the **types of data** linked to you or used for tracking, based on our disclosures and the App’s behavior (location, identifiers used for trial sync and analytics, etc.). The label is updated when we ship new versions that change data practices. This README is the detailed explanation; the label is the App Store summary.

### 10.4 When to contact Apple vs us

| Your question | Who to contact |
|---------------|----------------|
| Subscription charge, refund, or cancel on iPhone/iPad | **Apple** — Settings → Subscriptions, or [Report a Problem](https://reportaproblem.apple.com) |
| Apple ID, device, or iOS settings | **Apple Support** — [https://support.apple.com/](https://support.apple.com/) |
| What Within 10 stores, Firebase trial data, or this policy | **Us** — Section 12 (Contact) |
| Google Places, Firebase, or crash/analytics data we use | **Us** — Section 12; Google policies linked in Section 1 |

Apple is **not** responsible for the Within 10 application or our backend; we are the **data controller** for information described in Sections 1–5 that we (or Firebase on our behalf) process. Apple is an independent **platform and payment provider** for the iOS version.

---

## 11. Changes

We may update this policy when the App or legal requirements change. We will post the new version in this repository and update the “Last updated” date. Continued use after changes means you accept the updated policy.

---

## 12. Contact

**Privacy questions and requests:**

- Open an issue: [github.com/chamberton/Within10-Privacy-Policy/issues](https://github.com/chamberton/Within10-Privacy-Policy/issues)

Please include your platform (iOS/Android), App version (Settings → About), and a clear description of your request.

---

## 13. App Store disclosure (short form)

**Within 10 (iOS)** is distributed by Apple’s App Store. **Within 10** uses location to find nearby places and optional proximity alerts; contacts access only when you save or invite; local storage for favourites and cache; Google Places for search; Firebase for anonymous trial sync, analytics, and crash reports; **Apple (StoreKit)** / Google Play for subscriptions. No sale of personal data. No in-app ads. See [§10](#10-apple-privacy-and-services-ios) for Apple’s policies and support paths.
