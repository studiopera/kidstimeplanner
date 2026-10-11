# Privacy Policy

**App:** Kids Time Planner
**Data Controller:** Erhan Serin
**Contact:** studioperaturkey@gmail.com
**Effective date:** 31 May 2026
**Last updated:** 11 October 2026

> This policy is written in line with the EU General Data Protection
> Regulation (GDPR), the GDPR-K rules covering children under 16,
> Google Play Families Policy, and COPPA principles. A Turkish version
> is available at `/privacy-policy.tr`.

---

## 1. Summary

Kids Time Planner is a mobile app **designed for parents to manage their
children's daily task schedules**. Accounts are opened by parents; children
do not sign up themselves. A parent may optionally give a child a sign-in on
the child's own device (see 2.3). The app:

- Stores child data **only as entered by the parent** (name, emoji, task
  data).
- **Does not use child data for advertising** and does not sell or share it
  with third parties (other than the Google Firebase infrastructure provider).
- **Displays no ads** and contains no analytics or tracking SDKs (Firebase
  Analytics is currently disabled).

## 2. Data we collect

### 2.1 Parent (account holder) data

| Data | Source | Purpose | Retention |
|---|---|---|---|
| Email address | Signup form / Google Sign-In / Sign in with Apple | Account creation, authentication, password reset, OTP delivery | While the account is active |
| Display name | Signup / Google or Apple profile | In-app greeting | While the account is active |
| Password | Signup form | Authentication | Stored encrypted by Firebase; plain text is never stored |
| Premium subscription status | Google Play / Apple App Store | Access to premium features | While the account is active |
| FCM device token | Your device (Firebase Messaging) | Task completion notifications, weekly digest | Until the device is replaced or the account is deleted |
| PIN verifier | Local device setting | Restrict access to the parent panel | Local only (SharedPreferences); stored as a salted hash |

### 2.2 Child data (entered by the parent)

| Data | Purpose | Retention |
|---|---|---|
| Child name or nickname | Profile identification | Until the profile is deleted |
| Emoji / avatar choice | Visual identification | Until the profile is deleted |
| Tasks, completion logs, stars, rewards, routines | Core app functionality | While the account is active |

Child data is bound exclusively to the parent's Firebase UID. No other
parent can access this data (enforced server-side by Firestore Security Rules).

### 2.3 Child sign-in on the child's own device (optional)

A parent can let a child open **only that child's own profile** on another
phone or tablet. Nothing is created unless the parent turns this on for a
child profile in the parent panel.

| Data | Source | Purpose | Retention |
|---|---|---|---|
| Username and password chosen by the parent | Parent panel | Child sign-in | Until the parent removes the sign-in, deletes the profile, or deletes the account; the password is stored hashed by Firebase Auth |
| Child's own Apple, Google or email account (only if the parent sends an invitation to that email address) | Parent panel, then the child's sign-in | Child sign-in | Same as above; the email address in the invitation is kept only until it is accepted or removed |
| FCM device token of the child's device | Child's device | Task reminders on that device | Until sign-in is removed or the profile/account is deleted |

A child account can only read the tasks, rewards and goals of its own
profile and mark its own tasks as completed. It cannot open the parent
panel, make purchases, change settings, or see other children.

### 2.4 Automatically collected data

| Data | Purpose | Retention |
|---|---|---|
| Crash logs (Firebase Crashlytics) | Debugging | Firebase default (~90 days) |
| Device OS version (collected by Firebase) | Infrastructure compatibility | Firebase default |

The app does **not** collect location, contacts, microphone, calendar,
SMS, IMEI, or advertising identifiers.

## 3. Who we share data with

Your data is **not sold, rented, or shared with any advertising ecosystem**.
The following data processors are used solely to operate the service:

| Service provider | Data | Purpose | Agreement |
|---|---|---|---|
| Google Firebase (Auth, Firestore, Storage, Functions, Messaging) | All account & app data | Hosting and database | Google Data Processing Agreement (DPA) |
| Google Play Billing | Subscription receipt | Premium verification | Google Play Developer Agreement |
| Apple App Store (In-App Purchase) | Subscription receipt | Premium verification | Apple Developer Program License Agreement |
| Sign in with Apple | Email (may be a private relay address) + name | Login | Apple privacy policy |
| Google Sign-In | Email + name | One-tap login | Google Account policy |

We may disclose data to lawful authorities when legally required
(e.g., a court order).

## 4. Protecting children's data (important)

- The app complies with Google Play Families Policy and COPPA principles.
- Children cannot sign up by themselves. A child sign-in exists only if the
  parent creates it, is limited to that child's own profile, and can be
  removed by the parent at any time.
- Child data is **not processed for advertising** or profiled for analytics.
- The app shows **no ads to children** and contains no third-party
  advertising SDKs.
- The premium subscription purchase flow is **accessible only from the
  parent panel, protected by a PIN**; purchases cannot be initiated in
  child mode.

## 5. Where your data is stored

Data is stored encrypted on Google Cloud servers selected by Firebase
infrastructure. These servers may be located outside Türkiye (in the
European Union or United States). In this case, **international data
transfers** take place. Google secures such transfers under GDPR
Standard Contractual Clauses (SCCs).

## 6. Retention periods

- Data is retained while the account is active.
- When the parent removes a child sign-in or deletes a child profile, the
  related child sign-in account is deleted immediately.
- When the account is deleted, all user data (user document, child profiles,
  child sign-in accounts, task history, FCM tokens, OTP history) is permanently deleted
  **within 30 days**.
- Records subject to legal retention obligations (e.g., purchase receipts)
  are archived for the period required by law.

## 7. Your rights

Under GDPR Art. 15-22 (and equivalent local laws such as Turkey's KVKK
Art. 11) you have the right to:

- **Access** your data and request a copy
- Request **correction** of inaccurate or incomplete data
- Request **deletion** ("right to be forgotten")
- Request **restriction** of processing
- Object to **automated decision-making / profiling**
- File a complaint with a competent data protection authority

To exercise these rights: email **studioperaturkey@gmail.com** or use
the **Settings → Delete my account** option inside the app. We respond
to requests within **30 days**.

## 8. Security

- All traffic is encrypted with TLS (HTTPS).
- Firestore Security Rules enforce that users can only access their own
  data; cross-account access is denied server-side.
- Passwords are hashed with bcrypt by Firebase Auth; plain text passwords
  are never visible.
- The parent PIN is hashed on-device with SHA-256 + salt + 10,000 PBKDF2
  iterations.
- OTP codes are kept only as a **hash** in memory; the plain code is not
  persisted on-device after delivery.
- Purchase validation happens **server-side** (Cloud Function) via the
  Play Developer API; the client cannot write the `isPremium` field.

## 9. Cookies and tracking

The app runs on mobile platforms and does not use web cookies. It does
not include advertising or analytics tracking SDKs. Only the following
local storage mechanisms are used on-device:

- **SharedPreferences** (local settings, PIN hash, theme choice, streak)
- **Firebase local cache** (for offline functionality)

## 10. Changes to this policy

We may update this policy from time to time. Material changes will be
announced in advance via in-app notification or email. The "Last updated"
date above will reflect the latest revision.

## 11. Contact

For questions, requests, or complaints:

**Erhan Serin**
Email: studioperaturkey@gmail.com

---

*This document is informational and does not constitute legal advice.
If in doubt, consult a qualified lawyer or your local data protection
authority.*
