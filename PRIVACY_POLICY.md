# PocketMind AI — Privacy Policy

**Last updated: April 2026**
**App version: 1.0 and later**

---

## 1. Overview

PocketMind AI ("PocketMind", "we", "our", or "us") is a privacy-first personal finance application. This Privacy Policy explains what data we collect, how we use it, and your rights over it.

**Our core commitment:** Your financial data is stored locally on your device. We do not require bank credentials. We do not sell your data to third parties. We do not run advertising.

---

## 2. Data We Collect and Where It Is Stored

### 2.1 Data Stored Locally on Your Device Only

The following data is created by you and stored **only on your device** using SQLite (server-side) or device storage (client-side). It never leaves your device except as described in Section 2.2.

| Data type | What it contains | Where stored |
|---|---|---|
| Expenses | Date, amount, description, category, source | SQLite on your device / Render server tied to your anonymous ID |
| Savings Goals | Goal name, target amount, saved amount, contributions, icon, colour, deadline | Device (AsyncStorage via Zustand) |
| Budget settings | Monthly budget, per-category limits | Device + server (anonymous user record) |
| Category preferences | Patterns you've taught the app (e.g. "trader joe → Groceries") | Server (anonymous user record) |
| Streak data | Current streak count, longest streak, last log date | Device (AsyncStorage) |
| Badge/achievement data | Which badges you've earned, computed from your expense history | Device (AsyncStorage) |
| Financial Health Score | Computed locally from your expenses + budget. Never transmitted | Device only |
| Notification settings | Your preferences for alerts (on/off, daily prompt time) | Device (AsyncStorage) |

### 2.2 Data Sent to Third-Party Services

The following data is sent to third-party services **only when you use specific features**, and is **processed but not retained** by those services:

| Feature | Data sent | Service | Retention |
|---|---|---|---|
| AI text parsing ("Type" mode) | Your typed expense description | OpenAI API | Not stored per OpenAI's API data policy |
| Voice transcription | Your audio recording | OpenAI Whisper API | Not stored per OpenAI's API data policy |
| Receipt scanning | Your receipt photo (JPEG) | OpenAI Vision API | Not stored per OpenAI's API data policy |
| AI Advisor chat | Your question + anonymised expense summary | OpenAI API | Not stored per OpenAI's API data policy |
| AI Summary | Anonymised expense list | OpenAI API | Not stored per OpenAI's API data policy |
| Subscription detection | Anonymised expense list | OpenAI API | Not stored per OpenAI's API data policy |

**We do not send:** your name, email, phone number, bank details, location, device identifiers, or any information that could directly identify you to OpenAI or any other third party.

For OpenAI's data handling practices, see: https://openai.com/policies/api-data-usage-policies

### 2.3 Anonymous User Identifier

When you first launch PocketMind, a random UUID is generated and stored locally. This ID is used to associate your expense records on our server (hosted on Render.com). It is:
- Not linked to your name, email, Apple ID, or any identity
- Not shared with advertising networks
- Used solely to retrieve your own data

---

## 3. Push Notifications (Added in v1.0)

PocketMind may send you local push notifications for the following purposes:

| Notification type | Trigger | Can be disabled |
|---|---|---|
| Budget warning (80% used) | You reach 80% of your monthly budget | Yes — Settings → Notifications |
| Over-budget alert | You exceed your monthly budget | Yes — Settings → Notifications |
| Weekly spending recap | Every Sunday at 8pm | Yes — Settings → Notifications |
| Lapsed logging reminder | You haven't logged an expense in 2+ days | Yes — Settings → Notifications |
| Goal milestone | You reach 25%, 50%, 75%, or 100% of a savings goal | Yes — Settings → Notifications |
| Subscription reminder | A known subscription is due within 3 days | Yes — Settings → Notifications |
| Daily prompt (optional) | Time you choose in Settings | Disabled by default |

**All notifications are generated locally on your device.** No notification content is sent to our servers or any third party. We use `expo-notifications` which schedules notifications natively via iOS APNs and Android FCM — Apple and Google infrastructure handles delivery, but the content originates only from your device.

**Push notification permission:** We request notification permission on first launch. You can revoke it at any time in iOS Settings → PocketMind → Notifications.

---

## 4. Savings Goals Data

Savings Goals (introduced in v1.0) — including goal names, target amounts, saved amounts, and contributions — are stored **exclusively on your device** in AsyncStorage. This data:
- Is never transmitted to our server
- Is never shared with OpenAI or any third party
- Is included in your CSV export if you choose to export
- Is deleted when you use "Delete all my data" in Settings

---

## 5. Streak and Achievement Data

Your streak count, badge history, and Financial Health Score are computed entirely on-device from your local expense data. This data:
- Never leaves your device
- Is not shared with any third party
- Is reset if you use "Delete all my data" in Settings

---

## 6. Camera and Microphone Access

PocketMind requests the following device permissions only when you use the relevant features:

- **Camera** (`NSCameraUsageDescription`): Used only when you tap "Take photo" in receipt scanning mode. Photos are processed once by OpenAI Vision and are never stored on our servers.
- **Microphone** (`NSMicrophoneUsageDescription`): Used only when you hold the record button in voice entry mode. Audio is sent to OpenAI Whisper for transcription and is never stored on our servers.
- **Photo Library** (`NSPhotoLibraryUsageDescription`): Used only when you choose "Choose from gallery" in receipt scanning mode.

You can revoke any permission at any time in iOS Settings → PocketMind.

---

## 7. Data Retention and Deletion

- **On your device:** All data persists until you delete the app or use "Delete all my data" in Settings → Your Data.
- **On our server:** Your anonymous expense records are retained until you request deletion. To delete server-side data, use "Delete all my data" in the app, or email us at nkazi09@gmail.com with your anonymous User ID (visible in Settings → About).
- **OpenAI:** Audio and image data sent for processing is subject to OpenAI's API data retention policy. Per OpenAI's published API policy, API inputs and outputs are not used to train models and are retained for a limited period for abuse monitoring only.

---

## 8. Children's Privacy

PocketMind is not directed at children under 13. We do not knowingly collect data from children under 13. If you believe a child has used this app, please contact us at nkazi09@gmail.com.

---

## 9. Security

- All communication with our backend uses HTTPS (TLS)
- Your anonymous user ID and expense data are not accessible to other users
- We do not store payment information of any kind
- The app does not connect to your bank accounts

---

## 10. Third-Party Services Summary

| Service | Purpose | Privacy policy |
|---|---|---|
| OpenAI | AI parsing, voice transcription, receipt OCR, advisor chat | https://openai.com/policies/privacy-policy |
| Render.com | Backend hosting (anonymous expense storage) | https://render.com/privacy |
| Expo / React Native | App framework | https://expo.dev/privacy |
| Apple APNs | Push notification delivery (iOS) | https://www.apple.com/legal/privacy/ |

---

## 11. Your Rights

You have the right to:
- **Access** your data — export it as CSV from Settings → Your Data
- **Delete** your data — use "Delete all my data" in Settings, or email us
- **Opt out** of any notification type — Settings → Notifications
- **Withdraw camera/microphone consent** — iOS Settings → PocketMind

---

## 12. Changes to This Policy

If we make material changes to this policy (e.g. adding new data collection), we will update the "Last updated" date and notify you via an in-app message on next launch.

---

## 13. Contact

Questions about this Privacy Policy:

**Email:** nkazi09@gmail.com
**Support:** https://github.com/nkazi09/Privacy-Policy-PocketMind

---

*PocketMind AI is an independent application. It is not affiliated with, endorsed by, or connected to any financial institution.*
