# Within 10 — Privacy Policy

**Effective date:** 26 October 2026  
**Applies to:** Within 10 mobile application on **Apple iOS** and **Google Android** (including devices that use Google Mobile Services or, where applicable, Huawei Mobile Services for location).  
**Package / bundle ID:** `com.serge.mbamba.within10`  


This Privacy Policy describes how **Within 10** (“**we**”, “**us**”, “**the app**”) collects, uses, stores, and shares information when you use the app. It is written for users in all regions; additional rights may apply depending on where you live (see [Your rights](#your-rights)).

Within 10 helps you discover restaurants, hotels, bars, cafés, and other places near you (or near a location you choose), save favourites, plan trips, set up meetings, receive optional proximity alerts, and use optional on-device features such as food photo insights. **We do not sell your personal information and we do not show advertising in the app.**

---

## 1. Who is responsible for your data

The data controller for Within 10 is the developer and publisher of the app (Serge Mbamba / Within 10), reachable via the support URL above. For subscription billing, **Apple** (App Store) and **Google** (Google Play) process payments under their own privacy policies.

---

## 2. Summary

| Topic | What we do |
|--------|------------|
| **Location** | Used to find nearby places, simulate another area, navigation handoff, and (if you enable it) proximity alerts near saved places. Processed on your device; sent to **Google Places** only as needed to search places. |
| **Saved places & trips** | Stored **locally** on your device by default. Optional **cloud sync** uses Firebase for subscribed / trial users. |
| **Account** | **Anonymous Firebase sign-in** may be used to support trial and sync—not a public profile. |
| **Analytics & crashes** | **Firebase Analytics** (usage events) and **Firebase Crashlytics** (crash reports) in production builds. |
| **On-device AI** | Optional food insights run **on your device**; we do not upload those photos for cloud AI processing. |
| **Contacts** | Only if **you** invite people to meetings or save a place to contacts—via OS permission. |
| **Ads / tracking for ads** | **No ads.** On iOS we may ask for **App Tracking Transparency**; the app is designed to work if you decline. |
| **Children** | Not directed at children under 13 (or local minimum age). |

---

## 3. Information we collect

### 3.1 Information you provide

- **Saved favourites, collections, trips, meeting details, and notes** you create in the app.
- **Preferences** such as language, theme, place categories, sort order, and notification settings.
- **Meeting invitations** content you compose (recipients you select from your address book).
- **Exported data** when you use export features (files are created locally or via share sheets you control).

### 3.2 Information collected automatically

- **Precise and coarse location** (GPS and related signals) when you grant permission—while using the app and, if you opt in on Android/iOS, **in the background** for proximity alerts.
- **Simulated / manual location** when you choose to explore another area (treated like location for place searches).
- **Device and app identifiers** needed for subscriptions, trial eligibility, sync, and diagnostics—for example installation-scoped identifiers via Firebase and platform billing IDs (handled by Apple/Google for purchases).
- **Usage and performance data** via Firebase Analytics (e.g. searches, feature events) and Crashlytics (stack traces, device model, OS version).
- **Network and connectivity** status to load place data and sync when online.
- **Remote configuration** values from Firebase Remote Config (feature flags, limits)—no personal content.

### 3.3 Information from third-party services

- **Google Places / Maps APIs:** When you search or open place details, we send queries that include **location coordinates** (your real or simulated location) and place identifiers to Google to retrieve listings, photos, ratings, hours, and similar **public business information**. Google’s use of data is governed by [Google’s Privacy Policy](https://policies.google.com/privacy) and [Google Maps Platform Terms](https://cloud.google.com/maps-platform/terms).
- **Apple / Google Play:** Subscription status, receipts, and refund handling are processed by the store; we receive entitlement signals, not your full payment card number.

### 3.4 Information we do not collect for advertising

We do **not** use your data to serve third-party ads or to build advertising profiles. We do **not** sell personal information.

---

## 4. How we use information

We use information to:

1. **Provide core functionality** — show nearby places, maps, details, navigation links, favourites, trips, and meetings.  
2. **Optional proximity notifications** — alert you when you approach a saved place (requires location permission, including background where applicable).  
3. **Subscriptions and trials** — validate **Within X Pro** / **Within X Pro Max**, free trial windows, and feature limits.  
4. **Cloud sync (premium-related)** — replicate certain saved data to Firebase Firestore under an anonymous user ID when sync runs.  
5. **Improve reliability** — crash reporting, error monitoring, and aggregated analytics.  
6. **Configure the app** — remote config for limits and features without shipping a new store build.  
7. **On-device food insights** — classify food in photos locally when you request it.  
8. **Comply with law** and enforce our terms where required.

**Legal bases (EEA/UK):** performance of a contract (providing the app), legitimate interests (security, analytics, product improvement), and **consent** where required (e.g. optional background location, contacts, notifications, ATT on iOS).

---

## 5. Local storage on your device

Most of your content (favourites, trips, cache, settings) is stored in a **local database (ObjectBox)** on your phone or tablet. You can **clear cached place data** from settings. Uninstalling the app removes local app data subject to platform backup rules (see below).

**Biometric lock (Face ID / Touch ID / Android biometrics):** If enabled for meetings or sensitive notes, authentication is handled by your **operating system**; we do not receive your biometric data.

---

## 6. Cloud services (Firebase / Google)

When online, the app may use **Google Firebase**:

| Service | Purpose | Typical data |
|---------|---------|----------------|
| **Firebase Authentication** | Anonymous user ID for sync/trial | Anonymous UID, auth tokens |
| **Cloud Firestore** | Sync favourites and related sync payloads for entitled users | User-scoped documents under `users/{uid}/sync/...` |
| **Firebase Analytics** | Usage measurement | Events, app version, device class |
| **Firebase Crashlytics** | Crash diagnostics | Crash logs, device/OS metadata |
| **Firebase Remote Config** | Feature flags and limits | Config keys, no personal content |

Firebase is operated by **Google LLC**. Data may be processed in the United States or other countries where Google operates. See [Firebase Privacy](https://firebase.google.com/support/privacy).

Crashlytics collection is **disabled in debug/developer builds** where configured; production builds send crash reports to help us fix bugs.

---

## 7. Location — important details

- **When in use:** Location is used to list places around you, sort by distance, and open external map apps for directions.  
- **Simulated location:** You may set a different point on the map to explore another city; that coordinate is used in place searches sent to Google.  
- **Background location (optional):** If you enable proximity alerts, the app may access location while in the background (iOS *Background Modes: location*; Android *ACCESS_BACKGROUND_LOCATION* where granted). You can turn this off in system settings or in-app notification settings.  
- **Geofencing:** We register geofences around saved places to trigger notifications when you enter the configured radius.  
- **Huawei devices:** On some Android devices without Google Play services, **Huawei location services** may be used for location features instead of or in addition to Google Play services.

We do **not** claim to store your “live GPS trail” on our servers for tracking; location is used to provide features and place API requests as described.

---

## 8. Contacts, photos, and communications

- **Contacts (read/write):** Used only when **you** pick contacts for meeting invites or save a place entry to your address book. We do not upload your full contact list to our servers for marketing.  
- **Photos:** Place photos are loaded from Google Places or cached locally. **Food insight** uses photos you view in the app and processes them **on-device** with a local model; do not rely on it for medical or allergy decisions (results are AI-generated and may be wrong).  
- **Email / share sheets:** If you share exports or invitations, delivery goes through **your** chosen apps (Mail, Messages, etc.).

---

## 9. Notifications

With your permission, we send **local notifications** (e.g. proximity to a saved place). Notification content is derived from places **you** saved. You can disable notifications in app or system settings.

---

## 10. Subscriptions and in-app purchases

**Within X Pro** and **Within X Pro Max** are auto-renewing subscriptions processed by **Apple App Store** or **Google Play**. We receive purchase/entitlement status from the store SDK; we do not collect or store your payment card details.

**Restore purchases** uses the store’s restore flow. Legacy “remove ads” products may still restore entitlements for existing buyers.

**In-app review** prompts may be shown via Apple/Google review APIs; no personal review text is sent to us through that API.

---

## 11. Permissions (platform)

Permissions are requested when a feature needs them. Denying a permission may limit that feature but much of the app still works.

### Apple iOS (examples)

| Permission | Why |
|------------|-----|
| Location (When In Use / Always) | Nearby places, simulation, proximity alerts |
| Contacts | Meeting invites, save to contacts |
| Photo Library | Saving or accessing images where supported |
| Face ID | Optional lock for meetings/private notes |
| Notifications | Proximity alerts |
| App Tracking Transparency | Optional; app works if you deny; we do not use data for ads |

### Google Android (examples)

| Permission | Why |
|------------|-----|
| Fine / coarse location | Nearby places and distance |
| Background location | Optional proximity alerts |
| Contacts | Meeting invites, save to contacts |
| Internet / network state | Places API, sync, config |
| Notifications (Android 13+) | Proximity alerts |
| Biometric | Optional app/meeting lock |
| Activity recognition / related | Geofencing reliability on some devices |
| Storage (legacy paths) | Exports/cache where applicable on older API levels |

Exact permission names may vary by OS version. The system dialog text shown at runtime is authoritative.

---

## 12. Sharing and disclosure

We share information only:

- **With Google** (Places/Maps, Firebase) as needed to operate the app.  
- **With Apple or Google** for billing and subscription validation.  
- **With OS services** you invoke (Maps, Phone, Mail, Contacts).  
- **When required by law**, court order, or to protect rights, safety, and security.  
- **In connection with a merger or sale** of the app or its assets, with notice where required.

We do **not** share personal information with data brokers or ad networks for advertising.

---

## 13. Retention

- **On device:** Until you delete data in-app, clear cache, or uninstall.  
- **Firestore sync:** Retained while your anonymous account and sync documents exist; you may request deletion via contact below.  
- **Analytics / crash logs:** Retained per Google Firebase default retention; used for diagnostics and trend analysis.  
- **Trial records:** Kept locally and may sync to enforce trial limits.

---

## 14. Security

We use industry-standard measures including encrypted transport (HTTPS), platform secure storage where appropriate (e.g. keychain/Keystore for sensitive tokens), and least-privilege access to cloud data scoped by user ID. No method of transmission or storage is 100% secure.

---

## 15. International transfers

If you use Within 10 outside the country where our service providers host data (including the United States), your information may be transferred internationally. We rely on appropriate safeguards where required (e.g. provider terms and, where applicable, standard contractual clauses via Google/Firebase).

---

## 16. Your rights

Depending on your location, you may have the right to **access**, **correct**, **delete**, **restrict**, **object**, or **port** personal data, and to **withdraw consent** where processing is consent-based.

- **In-app:** Clear cache, delete saved items, revoke permissions in Settings, cancel subscriptions in the App Store / Play Store.  
- **Contact us** via [mailto:chamberton@hotmail.com) for access or deletion requests related to cloud sync data tied to your anonymous Firebase user (include app platform and approximate install date to help us locate records).

**California (CCPA/CPRA):** We do not sell personal information. You may request disclosure or deletion as above.

**EEA/UK GDPR:** You may lodge a complaint with your local supervisory authority.

---

## 17. Children

Within 10 is not intended for children under **13** (or the minimum age in your country without parental consent). We do not knowingly collect personal information from children. Contact us if you believe a child has provided data.

---

## 18. Third-party links and maps

The app opens **websites, maps, and review pages** operated by third parties (e.g. Google Maps, business sites). Their privacy practices apply once you leave Within 10 or use their apps.

---

## 19. Changes to this policy

We may update this Privacy Policy from time to time. We will post the revised version with a new **Effective date** and, where required, provide additional notice in the app or store listing. Continued use after changes means you accept the updated policy.

---

## 20. Platform-specific notes

### Apple App Store

- Privacy nutrition labels and App Store Connect disclosures should match this policy.  
- **Privacy Policy URL** in App Store Connect: [https://within10.app/privacy](https://within10.app/privacy) (or the URL you publish for this document).  
- **Apple’s Licensed Application End User License Agreement** applies to app use: [Apple Standard EULA](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/).

### Google Play

- Data safety form should align with sections 3–12 (location, contacts, analytics, crash data, optional background location, no ads).  
- **Short description / store listing** must remain consistent with this policy.

---

## 21. Contact

For privacy questions, requests, or complaints:

**Within 10**  
Email: [Email the developer](mailto:chamberton@hotmail.com)  
Raise and Issue: [Github issues] (https://github.com/chamberton/Within10-Privacy-Policy/issues)

We aim to respond to verified requests within a reasonable time and in accordance with applicable law.

---

*This document is the English master privacy policy for Within 10 on iOS and Android. Store listings in other languages are translations for convenience; if there is a conflict, the English version controls unless local law requires otherwise.*
