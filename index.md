# NativeKey Privacy Policy

**Last updated:** 2026-11-15

**Contact:** nativekey.support@gmail.com

This Privacy Policy describes how **NativeKey** (also referred to in product materials as **AIKey**), an Android custom keyboard app published by the NativeKey developer (`com.nativekey.keyboard`), handles information when you use the app.

NativeKey is a keyboard (input method). It lets you type into other apps, offers optional on-device suggestions and learning, and optional AI-assisted writing and translation when you choose to use those features. AI can run on-device, through NativeKey AI (a subscription-backed managed service), or through optional bring-your-own-key (BYOK) cloud providers.

---

## Summary

- **Normal typing** is processed on your device and sent only to the app you are typing into (the “host app”). Normal typing **does not** call AI services.
- **On-device AI (Gemini Nano)** — when available on your device and selected in Settings, AI-assisted Write and Read can process text **on your device**. For those on-device AI operations, the text processed for that AI request **does not leave your device** for cloud AI processing.
- **NativeKey AI (managed subscription)** — if you select NativeKey AI and explicitly start an AI action, selected, typed, or copied text plus the minimum request context is sent over **HTTPS** to the NativeKey backend and processed through NativeKey's managed AI infrastructure. A valid server-verified subscription entitlement is required.
- **Cloud AI (BYOK)** — if you choose a cloud provider (**Google Gemini**, **Anthropic Claude**, or **OpenAI**) and tap AI, selected, typed, or copied text may be sent over **HTTPS** to that provider using **your own API key**.
- **Local suggestions and learned words** stay on your device. They are not sent to AI providers. You can **clear learned suggestions** in Settings when you choose.
- **Sensitive fields** (such as passwords, banking apps, and similar protected contexts) disable AI, clipboard-based AI flows, suggestions, and local learning where intended.
- NativeKey **does not** include analytics SDKs, advertising SDKs, or permissions for contacts, location, camera, microphone, SMS, call logs, or broad storage access.
- NativeKey **does not sell** your personal data.

This policy is written to be accurate and conservative. It does **not** claim that no data ever leaves your device, because NativeKey AI and BYOK cloud AI features can transmit user-initiated AI text off-device when you choose those paths.

---

## 1. What NativeKey is

NativeKey is a third-party Android keyboard. When enabled in system settings, it can:

- Insert characters into text fields in other apps;
- Show optional **local** word suggestions;
- Optionally **learn** frequently used words and word pairs on your device;
- Optionally help you **rewrite, translate, or understand text** using **on-device AI** (when available), **NativeKey AI** (managed subscription), or **external BYOK cloud AI services** when you explicitly request AI.

Android shows a standard warning when any third-party keyboard is enabled. NativeKey is designed so that AI and clipboard reading for AI are not used during normal typing, and so that protected fields use a privacy-safe keyboard mode.

---

## 2. Information processed locally (on your device)

### 2.1 Normal typing

When you type without using AI:

- Keystrokes are handled on your device to display the keyboard and commit text to the active field in the host app.
- This normal typing flow **does not** send your text to NativeKey’s backend. NativeKey AI uses a backend only when you explicitly initiate an AI action with NativeKey AI selected.
- Normal typing **does not** call Gemini, Claude, OpenAI, or on-device AI APIs.

### 2.2 On-device AI (Gemini Nano)

When your device supports **Gemini Nano** (via Google ML Kit / Android AI Core) and you select **Gemini Nano** in **Settings → Connect your AI**:

- NativeKey may process text **on your device** for AI-assisted Write and Read when you tap AI.
- For those on-device AI operations, the text used for that AI request is processed locally and **does not leave your device** for cloud AI processing by NativeKey.
- On-device AI may require a one-time **model prepare/download** step managed by Google’s on-device AI components on your device.
- On-device AI availability depends on your device, Android version, and Google system components. It may be unavailable on some devices.

NativeKey does not send on-device AI request text to NativeKey’s own servers.

### 2.3 Local suggestions

NativeKey can suggest words from built-in word lists and from **on-device learning** (learned words and bigrams). Suggestions are generated locally. They are **not** sent to AI providers for suggestion ranking.

### 2.4 Local learning

When enabled and allowed for the current field, NativeKey may store learned word and bigram statistics locally (for supported keyboard languages) to improve future suggestions. This data remains on your device in app-private storage (`nativekey_suggestion_learning`).

You can delete this learned data at any time in **Settings → Privacy & Safety → Local suggestions → Clear learned suggestions**. That control removes locally learned words and word-pair (bigram) patterns only. It does **not** remove API keys, keyboard language settings, AI settings, or Keyboard Lab customization.

### 2.5 Settings and preferences

NativeKey stores settings locally (for example, keyboard layout choices, AI language preferences, and Keyboard Lab customization). These preferences are used to configure the keyboard on your device.

### 2.6 Privacy-safe / protected contexts

To reduce exposure of sensitive information, NativeKey detects certain **password**, **banking/finance**, and **password-manager** contexts using **field metadata and app identifiers** (such as input type flags, hints, and package or app label information)—**not** by uploading your typed content for classification.

In these protected contexts, NativeKey is intended to behave as a normal keyboard only: AI actions, clipboard reading for AI, local suggestions, local learning, and related features are disabled where designed.

---

## 3. Information that may leave your device

### 3.1 NativeKey AI (user-initiated managed service)

If you select **NativeKey AI** and explicitly use AI (for example, by tapping **AI**):

- NativeKey may send **text you selected or typed in the active field**, or clipboard text used by an incoming AI flow, plus request context such as source/target language and AI mode, over **HTTPS** to the NativeKey backend.
- The backend authenticates the app installation and checks a **server-verified NativeKey AI subscription entitlement** before allowing managed AI generation.
- The backend may forward the AI request content to a contracted AI service provider used to generate the response. The current managed AI backend uses **OpenAI** as its upstream AI provider.
- NativeKey AI does **not** use your personal Gemini, Claude, or OpenAI API key. Provider credentials for the managed service are held server-side.
- AI request/response content is processed for the requested operation. The backend may keep a **short-lived response cache for idempotency/retry protection** (currently designed with a short TTL, default 120 seconds) and does not use AI request text as a long-term typing-content database.
- The backend may retain operational metadata needed for authentication, subscription entitlement, quotas, abuse prevention, reliability, and cost/accounting, such as installation identifier, request identifier, route/mode, language settings, app version, latency, token usage, status, pricing version, and entitlement state.

For Google Play subscription verification, the app sends the **purchase token** to the NativeKey backend over HTTPS. The backend uses it transiently to verify the purchase with the Google Play Developer API and does not persist the raw purchase token. It stores a cryptographic hash and normalized entitlement metadata such as product, state, validity/expiry, and verification timestamps.

NativeKey currently has no conventional user account system for this flow; the service uses an app-installation identifier and authentication token to operate the backend entitlement and request controls.

### 3.2 Cloud AI-assisted features (user-initiated, BYOK)

If you select a **cloud AI provider**, configure an API key, and **explicitly use AI** (for example, by tapping **AI**):

- NativeKey may send **text you selected or typed in the active field**, plus related prompt/context needed for the request (such as source/target language settings), over **HTTPS** to:
  - **Google Gemini** (Google APIs),
  - **Anthropic Claude** (Anthropic APIs), or
  - **OpenAI** (OpenAI APIs),
  depending on the provider you selected in **Settings → Connect your AI**.

Cloud AI requests use **your** API key (**bring your own key / BYOK**). NativeKey does not provide cloud AI service accounts on your behalf.

**Outgoing AI** (rewrite/translate what you wrote): triggered when you ask for AI on text in the field.

**Incoming translation** (understand a copied message): may read **clipboard plain text** when you initiate the incoming/AI flow (for example, after copying a message and using AI). Clipboard content is not sent to AI in the background without your action.

If you use **on-device AI (Gemini Nano)** instead of a cloud provider, this off-device cloud transmission **does not occur** for that AI processing path.

If you do not configure cloud API keys, do not select a cloud provider, or you do not tap AI, cloud off-device transmission **does not occur** for AI processing.

### 3.3 What NativeKey does not control

When text is sent to **Google**, **Anthropic**, or **OpenAI** for BYOK cloud AI, or when NativeKey AI uses an upstream AI service provider, those providers process data under the applicable service terms and privacy/data-processing arrangements. NativeKey does not control independent provider-side retention outside NativeKey's own systems. Refer to:

- Google Gemini / Google API terms and privacy documentation (Google)
- Anthropic usage policies and privacy documentation (Anthropic)
- OpenAI API terms and privacy documentation (OpenAI)

On-device AI processing uses Google’s on-device AI components (ML Kit / AI Core). Google’s handling of model download, device-side inference, and related system services is governed by Google’s platform and service terms.

---

## 4. API keys (BYOK — cloud providers only)

Cloud AI features require an API key that **you** obtain from Google, Anthropic, or OpenAI.

- API keys are **stored locally** on your device in encrypted app-private storage where supported.
- Saved keys are **hidden in the UI**; the app does not display your key after you save it.
- Keys are sent to the selected cloud provider **only** as part of HTTPS API requests when you use cloud AI.
- You can remove keys in **Settings → Connect your AI** (**Clear key** per cloud provider). Removing a key stops further cloud AI requests to that provider from NativeKey.

**Gemini Nano (on-device AI)** does not require an API key. **NativeKey AI** also does not require you to provide a third-party API key because its managed provider credentials are server-side.

Treat API keys like passwords. Do not share them. You are responsible for usage and billing on your provider account.

NativeKey excludes certain preference files (including settings that may contain API keys and learned suggestion data) from Android cloud backup rules configured in the app, but you should assume keys remain on the device until cleared or the app is removed.

---

## 5. Clipboard

NativeKey may read **clipboard plain text on your device** when:

- You use **incoming** AI / translation flows that rely on copied text; and
- The current context is **not** a protected/sensitive field where clipboard reading is disabled.

NativeKey does not declare a separate Android clipboard permission; clipboard access uses standard platform APIs available to the keyboard when you initiate the relevant flow.

Clipboard text used for **NativeKey AI** may be transmitted to the NativeKey backend and managed AI infrastructure as described in Section 3.1. Clipboard text used for **BYOK cloud AI** may be transmitted to your selected cloud provider as described in Section 3.2. Clipboard text used for **on-device AI** is processed locally as described in Section 2.2.

---

## 6. Permissions and dependencies

NativeKey requests:

| Permission / dependency | Why |
|-------------------------|-----|
| `INTERNET` | Required for user-initiated NativeKey AI backend requests and for Gemini, Claude, and OpenAI BYOK cloud API requests |
| IME binding (`BIND_INPUT_METHOD`, system-enforced) | Required to function as a keyboard |

The app may also use **Google ML Kit Generative AI / Android AI Core** components for on-device AI. Merged dependencies may add system-level declarations such as `ACCESS_NETWORK_STATE` and access to Google AI Core services for model availability, download/prepare, and on-device inference. These support on-device AI and standard library operation; they do not change the on-device processing description in Section 2.2.

NativeKey does **not** request permissions for contacts, location, camera, microphone, SMS, call log, or broad external storage access.

---

## 7. Analytics, advertising, and sale of data

Based on the current app implementation:

- NativeKey **does not** integrate third-party **analytics** SDKs (for example, Firebase Analytics).
- NativeKey **does not** integrate **advertising** SDKs.
- NativeKey **does not sell** user personal data.
- NativeKey AI backend operational, entitlement, quota, security, and cost/accounting metadata is used to operate and protect the managed service; it is not an advertising profile.

If this changes in a future version, this policy will be updated before or alongside that release.

---

## 8. Data retention on your device

| Data | Typical retention |
|------|-------------------|
| Learned words/bigrams | Until you clear them in Settings (**Clear learned suggestions**), clear app data, or uninstall |
| Cloud API keys | Until you clear them in settings, app data cleared, or uninstall |
| AI-related settings | Until changed or app removed |
| NativeKey AI request/response text | Processed for the requested AI action; may be held in a short-lived backend idempotency/retry cache (currently designed with a short TTL, default 120 seconds), not as a long-term typing-content database |
| NativeKey AI entitlement/usage metadata | Retained as operationally needed for subscription verification, service access, quotas, security, reliability, and accounting; raw Google Play purchase tokens are not durably stored |
| Text sent directly to Gemini, Claude, or OpenAI (BYOK cloud AI) | Processed by those providers per **their** policies; not stored on NativeKey servers |
| On-device AI request text | Processed transiently on device during the request; not uploaded to NativeKey servers |

NativeKey does not operate a central database of your normal typing content. Off-device AI content is processed only when you explicitly initiate an AI flow using NativeKey AI or a BYOK cloud provider.

---

## 9. Your choices

You can:

- Use NativeKey **without AI** by not using AI features;
- Use **on-device AI** when available without adding a cloud API key;
- Use **NativeKey AI** only when you choose that provider and have an applicable subscription entitlement;
- **Remove cloud API keys** at any time in **Settings → Connect your AI** to stop BYOK cloud AI requests;
- **Clear learned suggestions** in Settings → Privacy & Safety to delete on-device learned words and word pairs;
- Avoid AI by not tapping the AI button;
- **Uninstall** the app to remove locally stored settings and learned data;
- Use Android system settings to disable or switch away from NativeKey as your keyboard.

For data held by Google, Anthropic, OpenAI, or another applicable AI service provider after an off-device AI request, provider-side controls depend on that provider and the applicable service relationship. For NativeKey-controlled backend data questions, contact NativeKey using the email in Section 13.

---

## 10. Children

NativeKey is not directed at children under 13 (or the minimum age required in your jurisdiction). We do not knowingly collect personal information from children through NativeKey.

---

## 11. International users

If you use **NativeKey AI**, request data may be processed where NativeKey's backend and managed AI service providers operate infrastructure. If you use **BYOK cloud AI**, text may be processed in countries where Google, Anthropic, or OpenAI operate infrastructure. Those off-device transfers occur only when you initiate the relevant AI flow.

On-device AI processing occurs on your device using Google’s on-device AI components.

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
- On-device AI, when available, can process text on your device without sending it to cloud AI providers for that operation;
- NativeKey AI, when selected, may send user-initiated AI text to the NativeKey backend and managed AI infrastructure and requires a server-verified subscription entitlement;
- BYOK cloud AI, when selected, may send text to your chosen provider only when you tap AI with your own API key;
- Protected fields disable AI and clipboard reading for AI;
- Local suggestions stay on the device;
- Learned suggestions can be cleared in Settings → Privacy & Safety.

If anything in the app disagrees with this hosted policy, treat this published Privacy Policy as the reference for store listing and Play Console purposes once a public URL is live—and update the app copy in a future release if needed.
