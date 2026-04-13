# Apple App Store — Privacy Nutrition Labels
# Go to: App Store Connect → Your App → App Privacy

## Question: Do you collect data from this app?
Answer: YES

---

## DATA TYPES TO DECLARE

### Financial Info
☑ CHECK "Other Financial Info"
- Used for: App Functionality
- Linked to identity: NO (anonymous UUID only)
- Used for tracking: NO

### Photos or Videos  
☑ CHECK "Photos or Videos"
- Used for: App Functionality (receipt scanning)
- Linked to identity: NO
- Used for tracking: NO

### Audio Data
☑ CHECK "Audio Data"
- Used for: App Functionality (voice expense entry)
- Linked to identity: NO
- Used for tracking: NO

### User Content
☑ CHECK "Other User Content" (expense descriptions)
- Used for: App Functionality
- Linked to identity: NO
- Used for tracking: NO

---

## DATA NOT COLLECTED (important — don't check these)
☐ Contact Info (no name, email, phone)
☐ Health & Fitness
☐ Location
☐ Contacts
☐ Browsing History
☐ Search History
☐ Identifiers > Advertising ID (you use UUID not IDFA)
☐ Purchases (you track user-entered expenses, not App Store purchases)
☐ Usage Data (no analytics SDK)
☐ Diagnostics (no crash reporting SDK — add Sentry if you want this)

---

## App Tracking Transparency (ATT)
Your app does NOT use the IDFA (Advertising Identifier) so you do NOT need to:
- Add NSUserTrackingUsageDescription to Info.plist
- Show the ATT permission prompt

This is a significant advantage — many apps lose users at the ATT prompt.

---

## IMPORTANT: NSUserTrackingUsageDescription
Do NOT add this key to your app.json infoPlist.
Your app does not track users across other apps/websites, so you don't need ATT.
Adding it unnecessarily would confuse Apple reviewers.

---

## Apple Review Notes (add these when submitting)
In the "Notes for App Review" field, paste this:

"SmartSpend AI uses an anonymous UUID (not linked to any personal identity)
to associate expenses with the user. No name, email, or contact information
is collected. Voice and receipt data is sent to OpenAI's API for processing
only and is not stored on any server. All financial data is stored locally
on the user's device or optionally on their own self-hosted backend.
The app does not use any advertising SDKs or tracking frameworks."

---

## App Store Required Links
1. Privacy Policy URL — must be live before submission
2. Support URL — can be your GitHub page or email (support@yourcompany.com)
3. Marketing URL — optional but recommended

---

## Common Rejection Reasons to Avoid

1. Microphone used without clear purpose shown to user
   → FIX: Your NSMicrophoneUsageDescription is already set ✅

2. Camera used without clear purpose
   → FIX: Your NSCameraUsageDescription is already set ✅

3. Privacy policy not accessible from within the app
   → FIX: Add a "Privacy Policy" link in your Settings screen (see fix below)

4. App crashes on first launch
   → FIX: Test on a clean simulator with no data ✅

5. Missing required functionality (app doesn't work without account)
   → FIX: Your app works fully offline ✅ (great for review)
