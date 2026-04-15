# Privacy Policy for PocketMind AI

**Last updated: April 2026**

## 1. Introduction

SmartSpend AI ("we", "our", or "the app") is committed to protecting your privacy. This policy explains what data we collect, how we use it, and your rights.

## 2. Data We Collect

### 2a. Data you provide
- **Expense descriptions** — text you type or speak describing purchases
- **Financial amounts and dates** — the numbers you log
- **Receipt photos** — images you choose to scan (processed immediately, never stored on our servers)
- **Voice recordings** — audio recorded when you use voice entry (processed immediately, never stored)
- **Budget preferences** — monthly budget and category limits you set

### 2b. Data we generate
- **Anonymous user ID** — a random identifier (UUID) created on first launch. This is NOT linked to your name, email, or any personal identity.

### 2c. Data we do NOT collect
- ❌ Name, email address, or phone number
- ❌ Bank account credentials or financial account access
- ❌ Location data
- ❌ Contact list
- ❌ Device advertising ID
- ❌ Browsing history

## 3. How We Use Your Data

| Data | Purpose | Third party involved |
|---|---|---|
| Expense text | AI parsing and categorisation | OpenAI API |
| Voice audio | Speech-to-text transcription | OpenAI Whisper API |
| Receipt photos | Merchant and amount extraction | OpenAI Vision API |
| All expense data | AI advisor responses, summaries | OpenAI API |
| Anonymous UUID | Linking your expenses on your own server | Your self-hosted backend only |

## 4. Third-Party Services

### OpenAI
Your expense text, voice audio, and receipt photos are sent to OpenAI's API for processing. OpenAI processes this data under their API data usage policy. As of March 2023, OpenAI does not use API data to train their models by default.
- OpenAI Privacy Policy: https://openai.com/privacy

**Important:** Audio and image data is sent to OpenAI only at the moment of processing and is not stored by SmartSpend on any server.

## 5. Data Storage

- All your expense data is stored on **your own device** (via local storage) and optionally on **your own self-hosted backend server**.
- We do not operate a central database containing your financial information.
- We do not sell your data to any third party.
- We do not use your data for advertising.

## 6. Permissions We Request

| Permission | Why we need it |
|---|---|
| Microphone | Voice expense entry — only active when you hold the record button |
| Camera | Receipt scanning — only activated when you tap "Take photo" |
| Photo library | Receipt scanning from existing photos — only when you tap "Choose from gallery" |
| Internet | Connecting to your backend server and OpenAI for AI features |

## 7. Data Retention

- Your expense data remains on your device until you delete the app or clear app data.
- OpenAI does not retain API inputs beyond the immediate processing request (per their API policy).
- We do not have access to delete your data because we do not store it centrally.

## 8. Children's Privacy

SmartSpend AI is not directed at children under 13. We do not knowingly collect data from children.

## 9. Your Rights

Depending on your location, you may have rights to:
- Access the data stored about you (it's on your device — open the app)
- Delete your data (delete the app or clear app storage)
- Export your data (use the CSV export feature in Settings)

## 10. Changes to This Policy

We will notify users of material changes by updating the "Last updated" date above.

## 11. Contact

For privacy questions: nkazi09@gmail.com
