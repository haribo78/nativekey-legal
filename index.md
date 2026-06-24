# NativeKey Privacy Policy

**Last updated:** 2026-06-24

**Contact:** nativekey.support@gmail.com

This Privacy Policy describes how **NativeKey** (also referred to in product materials as **AIKey**), an Android custom keyboard app published by the NativeKey developer (`com.nativekey.keyboard`), handles information when you use the app.

NativeKey is a keyboard (input method). It lets you type into other apps, offers optional on-device suggestions and learning, and optional AI-assisted writing and translation when you choose to use those features.

---

## Summary

- **Normal typing** is processed on your device and sent only to the app you are typing into (the “host app”). Normal typing **does not** call AI services.
- **AI features** run **only when you ask for them** (for example, by tapping the AI button). When you use AI, selected, typed, or copied text may be sent over **HTTPS** to the AI provider you selected (Google **Gemini**, Anthropic **Claude**, or **OpenAI**), using **your own API key**.
- **Local suggestions and learned words** stay on your device. They are not sent to AI providers. You can **clear learned suggestions** in Settings when you choose.
- **Sensitive fields** (such as passwords, banking apps, and similar protected contexts) disable AI, clipboard-based AI flows, suggestions, and local learning where intended.
- NativeKey **does not** include analytics SDKs, advertising SDKs, or permissions for contacts, location, camera, microphone, SMS, call logs, or broad storage access.
- NativeKey **does not sell** your personal data.

This policy is written to be accurate and conservative. It does **not** claim that no data ever leaves your device, because AI features can transmit text to third-party providers when you initiate them.

---

## 1. What NativeKey is

NativeKey is a third-party Android keyboard. When enabled in system settings, it can:

- Insert characters into text fields in other apps;
- Show optional **local** word suggestions;
- Optionally **learn** frequently used words and word pairs on your device;
- Optionally help you **rewrite, translate, or understand text** using external AI services when you explicitly request AI.

Android shows a standard warning when any third-party keyboard is enabled. NativeKey is designed so that AI and clipboard reading for AI are not used during normal typing, and so that protected fields use a privacy-safe keyboard mode.

---

## 2. Information processed locally (on your device)

### 2.1 Normal typing

When you type without using AI:

- Keystrokes are handled on your device to display the keyboard and commit text to the active field in the host app.
- This typing flow **does not** send your text to NativeKey’s own servers (NativeKey does not operate backend servers for typing).
- Normal typing **does not** call Gemini, Claude, OpenAI, or other AI APIs.

### 2.2 Local suggestions

NativeKey can suggest words from built-in word lists and from **on-device learning** (learned words and bigrams). Suggestions are generated locally. They are **not** sent to AI providers for suggestion ranking.

### 2.3 Local learning

When enabled and allowed for the current field, NativeKey may store learned word and bigram statistics locally (for supported keyboard languages) to improve future suggestions. This data remains on your device in app-private storage (`nativekey_suggestion_learning`).

You can delete this learned data at any time in **Settings → Privacy & Safety → Local suggestions → Clear learned suggestions**. That control removes locally learned words and word-pair (bigram) patterns only. It does **not** remove API keys, keyboard language settings, AI settings, or Keyboard Lab customization.

### 2.4 Settings and preferences

NativeKey stores settings locally (for example, keyboard layout choices, AI language preferences, and Keyboard Lab customization). These preferences are used to configure the keyboard on your device.

### 2.5 Privacy-safe / protected contexts

To reduce exposure of sensitive information, NativeKey detects certain **password**, **banking/finance**, and **password-manager** contexts using **field metadata and app identifiers** (such as input type flags, hints, and package or app label information)—**not** by uploading your typed content for classification.

In these protected contexts, NativeKey is intended to behave as a normal keyboard only: AI actions, clipboard reading for AI, local suggestions, local learning, and related features are disabled where designed.

---

## 3. Information that may leave your device

### 3.1 AI-assisted features (user-initiated)

If you configure an API key and **explicitly use AI** (for example, by tapping **AI**):

- NativeKey may send **text you selected or typed in the active field**, plus related prompt/context needed for the request (such as source/target language settings), over **HTTPS** to:
  - **Google Gemini** (Google APIs),
  - **Anthropic Claude** (Anthropic APIs), or
  - **OpenAI** (OpenAI APIs),
  depending on the provider you selected in **Settings → AI Engine**.

AI requests use **your** API key (**bring your own key / BYOK**). NativeKey does not provide AI service accounts on your behalf.

**Outgoing AI** (rewrite/translate what you wrote): triggered when you ask for AI on text in the field.

**Incoming translation** (understand a copied message): may read **clipboard plain text** when you initiate the incoming/AI flow (for example, after copying a message and using AI). Clipboard content is not sent to AI in the background without your action.

If you do not configure API keys, or you do not tap AI, this off-device transmission **does not occur** for AI processing.

### 3.2 What NativeKey does not control

When text is sent to **Google**, **Anthropic**, or **OpenAI**, those companies process it under **their** terms and privacy policies. NativeKey **does not** operate those services and **cannot** guarantee how long they retain data, how they use it beyond your API request, or whether you can delete data from their systems. Refer to:

- Google Gemini / Google API terms and privacy documentation (Google)
- Anthropic usage policies and privacy documentation (Anthropic)
- OpenAI API terms and privacy documentation (OpenAI)

---

## 4. API keys (BYOK)

AI features require an API key that **you** obtain from Google, Anthropic, or OpenAI.

- API keys are **stored locally** on your device in app-private storage (SharedPreferences).
- Saved keys are **hidden in the UI**; the app does not display your key after you save it.
- Keys are sent to the selected provider **only** as part of HTTPS API requests when you use AI.
- You can remove keys in **Settings → AI Engine** (**Clear key** per provider). Removing a key stops further AI requests to that provider from NativeKey.

Treat API keys like passwords. Do not share them. You are responsible for usage and billing on your provider account.

NativeKey excludes certain preference files (including settings that may contain API keys and learned suggestion data) from Android cloud backup rules configured in the app, but you should assume keys remain on the device until cleared or the app is removed.

---

## 5. Clipboard

NativeKey may read **clipboard plain text on your device** when:

- You use **incoming** AI / translation flows that rely on copied text; and
- The current context is **not** a protected/sensitive field where clipboard reading is disabled.

NativeKey does not declare a separate Android clipboard permission; clipboard access uses standard platform APIs available to the keyboard when you initiate the relevant flow.

Clipboard text used for AI may be transmitted to your selected AI provider as described in Section 3.

---

## 6. Permissions

NativeKey requests:

| Permission | Why |
|------------|-----|
| `INTERNET` | Required to call Gemini, Claude, and OpenAI APIs when **you** use AI |
| IME binding (`BIND_INPUT_METHOD`, system-enforced) | Required to function as a keyboard |

NativeKey does **not** request permissions for contacts, location, camera, microphone, SMS, call log, or broad external storage access.

---

## 7. Analytics, advertising, and sale of data

Based on the current app implementation:

- NativeKey **does not** integrate third-party **analytics** SDKs (for example, Firebase Analytics).
- NativeKey **does not** integrate **advertising** SDKs.
- NativeKey **does not sell** user personal data.

If this changes in a future version, this policy will be updated before or alongside that release.

---

## 8. Data retention on your device

| Data | Typical retention |
|------|-------------------|
| Learned words/bigrams | Until you clear them in Settings (**Clear learned suggestions**), clear app data, or uninstall |
| API keys | Until you clear them in settings, app data cleared, or uninstall |
| AI-related settings | Until changed or app removed |
| Text sent to Gemini, Claude, or OpenAI | Processed by those providers per **their** policies; not stored on NativeKey servers |

NativeKey does not operate a central database of your typing content.

---

## 9. Your choices

You can:

- Use NativeKey **without AI** by not adding API keys;
- **Remove API keys** at any time in **Settings → AI Engine** to stop AI requests;
- **Clear learned suggestions** in Settings → Privacy & Safety to delete on-device learned words and word pairs;
- Avoid AI by not tapping the AI button;
- **Uninstall** the app to remove locally stored settings and learned data;
- Use Android system settings to disable or switch away from NativeKey as your keyboard.

For data held by Google, Anthropic, or OpenAI after an AI request, follow those providers’ account and support processes.

---

## 10. Children

NativeKey is not directed at children under 13 (or the minimum age required in your jurisdiction). We do not knowingly collect personal information from children through NativeKey.

---

## 11. International users

If you use AI features, text may be processed in countries where Google, Anthropic, or OpenAI operate infrastructure. Those transfers are initiated by **your** use of AI with **your** API key.

---

## 12. Changes to this policy

We may update this Privacy Policy from time to time. The **Last updated** date at the top will change when we do. For material changes, we will provide notice in the app or on the published policy page where feasible.

---

## 13. Contact

Questions about this Privacy Policy:

**Email:** nativekey.support@gmail.com

---

## 14. Relationship to in-app disclosures

NativeKey includes in-app **Privacy & Safety** explanations (Settings and onboarding) that summarize:

- Normal typing stays on the device and does not call AI;
- AI runs only when you tap AI;
- Protected fields disable AI and clipboard reading for AI;
- Local suggestions stay on the device;
- Learned suggestions can be cleared in Settings → Privacy & Safety.

If anything in the app disagrees with this hosted policy, treat this published Privacy Policy as the reference for store listing and Play Console purposes once a public URL is live—and update the app copy in a future release if needed.
