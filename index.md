# Privacy Policy for NativeKey

**Last updated: 2026-11-15**

**Contact:** nativekey.support@gmail.com

This Privacy Policy explains how NativeKey, an Android custom keyboard app published under the package name `com.nativekey.keyboard`, handles information when you use the app.

NativeKey is a keyboard input method. It lets you type into other apps, provides optional on-device suggestions and learning, and offers optional AI-assisted writing, rewriting, translation, and understanding features.

## Summary

- Normal typing is processed on your device and sent only to the app you are typing into, also called the host app.
- Normal typing does not call an AI service.
- Local suggestions and learned words stay on your device.
- On supported devices, NativeKey can use on-device AI powered by Gemini Nano through Android system services. In this mode, the prompt and result are processed on the device and are not sent to a cloud AI provider for inference.
- Cloud AI features run only when you explicitly request them. NativeKey supports bring-your-own-key (BYOK) cloud providers and may also provide a first-party managed cloud option called NativeKey AI.
- With NativeKey AI, the requested text is sent over HTTPS to a NativeKey-operated backend, which sends the request to the configured AI inference provider. You do not need to supply your own provider API key for this mode.
- NativeKey AI uses a random installation identifier and short-lived authentication token. The backend keeps technical metadata for security, quota, reliability, and cost accounting. It is not designed to keep your normal typing content as long-term history.
- Clipboard text is used for incoming translation or similar AI flows only when you start that flow.
- Protected contexts such as passwords, banking apps, and similar sensitive fields disable AI, clipboard-based AI flows, suggestions, and local learning where designed.
- NativeKey supports optional one-time purchases through Google Play Billing.
- Google Play handles payment transactions. NativeKey does not receive or store payment-card numbers, bank-account details, or full payment credentials.
- NativeKey stores only local purchase-entitlement information needed to show whether each product is purchased, pending, or not currently verified as owned.
- Purchase tokens are not stored in NativeKey’s entitlement preferences and are not sent to a NativeKey-operated server.
- NativeKey does not include advertising SDKs or third-party analytics SDKs.
- NativeKey does not sell personal data.
- NativeKey does not create or require a NativeKey user account.
- NativeKey does not operate a central database of your typing content.
- NativeKey never sends messages automatically.
- This policy does not claim that no data ever leaves your device. Text can leave the device when you explicitly use a cloud AI provider, and purchase-related technical information is exchanged with Google Play when Billing features are used.

## 1. What NativeKey is

NativeKey is a third-party Android keyboard. When enabled in Android system settings, it can:

- insert characters into text fields in other apps;
- show optional local word suggestions;
- optionally learn frequently used words, correction choices, and word pairs on your device;
- optionally help you write, rewrite, translate, or understand text;
- use supported on-device AI, a cloud AI provider that you configure with your own key, or the NativeKey AI managed cloud service when available;
- offer optional one-time purchases through Google Play.

Android displays a standard warning when any third-party keyboard is enabled. NativeKey is designed so that normal typing does not call AI services and protected fields use a privacy-safe keyboard mode.

NativeKey does not automatically send messages, submit forms, or press a host app’s Send button.

## 2. Information processed locally on your device

### 2.1 Normal typing

When you type without using AI:

- keystrokes are handled on your device to display the keyboard and commit text to the active field in the host app;
- this typing flow does not send your text to NativeKey-operated servers;
- normal typing does not call Gemini, Claude, OpenAI, or another cloud AI API.

The host app receives the text you enter because that is the purpose of the keyboard.

### 2.2 Local suggestions

NativeKey can suggest words from built-in word lists and from on-device learning. Suggestion generation and ranking are performed locally.

Local suggestions are not sent to cloud AI providers for ranking.

### 2.3 Local learning

When enabled and allowed for the current field, NativeKey may store local statistics such as learned words, correction choices, and word-pair patterns to improve future suggestions.

This information remains in app-private storage on your device.

You can delete learned suggestion data in:

`Settings → Privacy & Safety → Local suggestions → Clear learned suggestions`

This control removes locally learned suggestion data. It does not remove API keys, keyboard language choices, AI settings, purchase-entitlement records, or Keyboard Lab customization.

### 2.4 Settings and preferences

NativeKey stores settings locally, including:

- keyboard layouts and enabled languages;
- typing and feedback preferences;
- AI language and provider settings;
- Keyboard Lab customization;
- privacy and safety settings;
- other app preferences required to provide the selected behavior.

### 2.5 On-device AI

On supported devices, NativeKey can use Gemini Nano through Android’s on-device AI system services and ML Kit GenAI APIs.

When on-device AI is selected:

- the prompt and result are processed on the device;
- NativeKey does not send that prompt to Google Gemini cloud, Anthropic, or OpenAI for inference;
- an API key is not required for the on-device request;
- availability depends on the device, Android system components, model readiness, and supported languages or capabilities.

Android or Google system services may download, update, prepare, or manage the on-device model and related components. Those system services are controlled by Google and Android and may handle technical service information under their own terms.

NativeKey does not receive your prompt through a NativeKey server.

Ownership of an On-device AI purchase does not determine whether a particular device technically supports Gemini Nano.

### 2.6 Privacy-safe and protected contexts

To reduce exposure of sensitive information, NativeKey checks local field metadata and app context, such as input type flags, field hints, package names, and app labels.

This detection is performed locally and does not upload your typed content for classification.

In protected contexts, NativeKey is intended to operate as a normal keyboard only. AI actions, clipboard reading for AI, local suggestions, local learning, and related features are disabled where designed.

### 2.7 Local purchase-entitlement records

NativeKey stores a local record of Google Play purchase status so that the app can show whether each optional product is:

- purchased;
- pending;
- not currently verified as owned.

The current implementation keeps separate entitlement records for:

- On-device AI Lifetime;
- BYOK Lifetime, which relates to use of your own supported AI-provider API key;
- NativeKey AI Pro, a Google Play subscription for the NativeKey-managed AI service.

These products are independent. Ownership of either Lifetime product does not automatically create a NativeKey AI Pro subscription, and a NativeKey AI Pro subscription does not create Lifetime ownership.

The local purchase record may contain:

- whether each product is recorded as owned;
- whether each product is pending;
- the last verification time for each product;
- the time of the last successful Google Play purchase query;
- the result of the most recent purchase query.

The local purchase record does not contain:

- payment-card numbers;
- bank-account details;
- full payment credentials;
- Google Play order IDs;
- a saved Google account email address;
- a persistent purchase token.

NativeKey excludes its lifetime-entitlement preference file from the Android cloud-backup and device-transfer rules configured by the app.

## 3. Information that may leave your device

### 3.1 Cloud AI features

Cloud AI features are optional and run only after you explicitly start an AI action.

NativeKey supports two cloud AI paths:

#### BYOK cloud AI

If you choose a supported provider and save your own API key, NativeKey may send the following directly over HTTPS to that provider:

- selected text;
- text you typed for the requested AI action;
- copied clipboard text used for an incoming AI flow;
- source and target language choices;
- instructions needed to complete the requested AI action;
- the API key required by the selected provider.

Supported BYOK providers may include:

- Google Gemini;
- Anthropic Claude;
- OpenAI.

Your API key is used only for the provider you selected.

#### NativeKey AI managed cloud service

When NativeKey AI is available and selected, you do not provide your own AI-provider API key.

After you explicitly start a NativeKey AI action, NativeKey may send the following over HTTPS to a NativeKey-operated backend:

- the text needed for the requested rewrite or translation;
- source and target language choices;
- the selected tone;
- a fixed message style used by the app;
- app version and version code;
- a random installation identifier and request identifier used for authentication, quota, abuse prevention, and request handling.

The NativeKey backend constructs the AI prompt and sends the request to the configured inference provider. The current managed service may use OpenAI.

The NativeKey backend is designed not to log input text, output text, prompts, clipboard text, API keys, or authorization headers in its application logs.

For reliability and duplicate-request protection, a completed NativeKey AI response may be stored temporarily in a short-lived idempotency cache and then expired and purged. This cache is not intended as conversation history or long-term content storage.

The backend may retain technical metadata such as:

- random installation identifier;
- request identifier;
- AI mode;
- source and target language metadata;
- app version and version code;
- request count and quota state;
- input and output token counts;
- model route;
- latency;
- status or normalized error information;
- timestamps needed for security, operations, and accounting.

NativeKey AI does not require a NativeKey user account.

Outgoing AI actions, such as rewriting or translating text you wrote, run only after you explicitly request the action.

Incoming AI actions, such as translating copied text, may read clipboard plain text only after you initiate the incoming AI flow.

If you do not start a cloud AI action, cloud AI transmission does not occur.

### 3.2 Third-party AI providers

When text is sent to Google, Anthropic, OpenAI, or another configured inference provider, that provider processes it under its own terms, privacy policy, and service settings. This applies whether the request is sent directly in BYOK mode or through the NativeKey AI managed backend.

NativeKey does not operate those services and cannot guarantee:

- how long a provider retains a request;
- whether a provider uses request data for service improvement;
- which account-level privacy controls are available;
- whether NativeKey can delete data from that provider’s systems.

For requests concerning data held by a cloud AI provider, use that provider’s account, privacy, and support processes.

### 3.3 Google Play Billing

NativeKey uses Google Play Billing for optional one-time purchases and for the NativeKey AI Pro subscription.

When Billing features are used, NativeKey communicates with Google Play to:

- connect to the Google Play Billing service;
- retrieve available one-time products and subscription products;
- retrieve localized product, base-plan, and offer information;
- start a purchase flow after your action;
- receive purchase updates;
- acknowledge eligible completed purchases;
- query active one-time purchases and subscriptions;
- restore or re-verify eligible purchases;
- reconcile locally stored purchase-entitlement records.

NativeKey may query Google Play when the NativeKey settings app starts or resumes, when purchase information needs to be refreshed, or when you choose Restore purchases.

NativeKey AI Pro uses server-side purchase verification. When you have a Google Play NativeKey AI Pro purchase, the app may send the Google Play purchase token over HTTPS to the NativeKey-operated backend. The backend uses that token only to verify or acknowledge the purchase with the Google Play Developer API.

The NativeKey backend does not intentionally log or persist the raw Google Play purchase token. It may retain a SHA-256 hash of the token together with limited subscription-entitlement metadata such as the product ID, verified subscription state, entitlement status, expiry time, verification time, and random installation identifier.

Google Play Billing operations do not include:

- your normal typed text;
- clipboard text;
- AI prompts or AI results;
- saved API keys;
- learned words;
- correction choices;
- keyboard layouts or customization.

Google Play handles the financial transaction under Google’s own terms and privacy practices.

## 4. API keys

BYOK cloud AI features require an API key obtained directly from the selected provider. NativeKey AI does not require you to provide your own inference-provider API key.

- API keys are stored locally in encrypted app-private storage using Android security APIs.
- Saved keys are hidden in the NativeKey interface.
- NativeKey does not intentionally send your API key to a NativeKey-operated server.
- A key is sent only to the selected provider as required for an HTTPS AI request.
- You can remove saved keys under `Settings → Connect your AI`.
- Removing a key stops future NativeKey requests to that provider unless a new key is saved.

Treat API keys like passwords. You are responsible for use, limits, and billing associated with your provider account.

NativeKey excludes certain preference files, including files that may contain API keys and learned suggestion data, from the Android cloud-backup rules configured by the app.

You should nevertheless assume that a saved key remains on the device until you remove it, clear app data, or uninstall NativeKey.

## 5. Clipboard

NativeKey may read clipboard plain text when:

- you start an incoming AI or translation flow that relies on copied text; and
- the current field is not a protected context where clipboard-based AI is disabled.

NativeKey does not declare a separate Android clipboard permission. Clipboard access uses Android platform APIs available to the keyboard in the relevant context.

Clipboard text used with on-device AI is processed on the device.

Clipboard text used with a cloud AI action may be sent either directly to the selected BYOK provider or to the NativeKey AI managed backend and its configured inference provider, as described in Section 3.

NativeKey does not send clipboard text to an AI provider in the background without your action.

## 6. Google Play purchases

### 6.1 Purchase types

NativeKey supports two independent optional one-time purchase products:

- **On-device AI Lifetime**;
- **BYOK Lifetime**, relating to use of your own supported AI-provider API key.

NativeKey does not currently offer subscriptions.

Prices are supplied by Google Play in localized form. NativeKey does not hardcode or calculate your payment details.

### 6.2 Information received from Google Play

For purchase, acknowledgement, and restore functionality, NativeKey may receive technical purchase information from Google Play, including:

- product identifiers;
- localized price and offer information;
- purchase state, such as purchased or pending;
- acknowledgement state;
- a purchase token required to process and acknowledge a purchase;
- Google Play Billing response and availability information.

NativeKey does not request or store:

- payment-card numbers;
- bank-account details;
- full payment credentials;
- the purchaser’s Google account email address;
- the purchaser’s full name;
- Google Play order IDs.

### 6.3 Purchase tokens

A Google Play purchase token may be handled temporarily in application memory when NativeKey receives, processes, or acknowledges a purchase.

NativeKey does not persist purchase tokens in its entitlement preferences.

NativeKey does not intentionally log purchase tokens.

NativeKey does not send purchase tokens to a NativeKey-operated server.

NativeKey currently does not operate a purchase-verification backend.

### 6.4 Pending purchases

A purchase reported by Google Play as pending is recorded as pending and is not recorded as purchased.

NativeKey waits until Google Play reports the purchase as completed before recording the related product as owned.

### 6.5 Purchase acknowledgement

After NativeKey receives an eligible completed purchase, it may acknowledge the purchase through Google Play.

Acknowledgement informs Google Play that the completed purchase has been processed by the app.

An acknowledgement error does not itself prove that the underlying purchase is invalid. A later Google Play query may return the purchase again and allow another acknowledgement attempt.

### 6.6 Restore purchases

Restore purchases performs a current query to Google Play for active purchases associated with the Google Play account currently used by Google Play on the device.

NativeKey does not grant restored ownership from the local cache alone.

If Google Play returns a successful purchase result:

- products reported as purchased are recorded as owned;
- products reported as pending remain pending and are not recorded as purchased;
- a product absent from a successful authoritative result may be recorded as not currently owned.

If Google Play is unavailable or returns an error, NativeKey preserves previously verified local ownership instead of treating the connection failure as proof that a purchase does not exist.

### 6.7 Clearing local purchase records

Clearing NativeKey app data or uninstalling NativeKey removes the local purchase-entitlement records.

This does not by itself cancel or refund a Google Play purchase.

Eligible purchases may be restored by querying Google Play again with the Google Play account used for the purchase.

## 7. Permissions and Android access

NativeKey declares the `INTERNET` permission so it can contact a selected BYOK cloud provider or the NativeKey AI managed backend when you explicitly use a cloud AI feature.

The NativeKey input-method service is protected by Android’s `BIND_INPUT_METHOD` system permission. This allows NativeKey to function as a keyboard and is controlled by Android.

NativeKey uses the Google Play Billing Library for purchase operations. The Billing Library supplies the Android manifest access required to communicate with Google Play Billing.

This Billing access does not give NativeKey access to payment-card numbers, bank-account details, or full payment credentials.

NativeKey does not request permissions for:

- contacts;
- location;
- camera;
- microphone;
- SMS;
- call logs;
- broad external storage access.

## 8. Analytics, advertising, and sale of data

Based on the current app implementation:

- NativeKey does not integrate third-party analytics SDKs;
- NativeKey does not integrate advertising SDKs;
- NativeKey does not sell personal data;
- NativeKey does not operate behavioral advertising or cross-app tracking;
- the NativeKey AI backend may process and retain privacy-safe technical metadata for authentication, quota enforcement, abuse prevention, reliability, and cost accounting, as described in Section 3.1.

If this changes in a future version, this policy and the Google Play Data Safety declaration will be updated before or alongside that release.

## 9. Data retention

### 9.1 Local typing and settings data

Learned words, correction choices, and word-pair patterns remain on your device until you:

- clear learned suggestions in NativeKey;
- clear NativeKey app data;
- uninstall NativeKey.

Saved API keys remain on your device until you:

- remove them in NativeKey settings;
- clear NativeKey app data;
- uninstall NativeKey.

Other local settings remain until changed, cleared, or removed with the app.

### 9.2 Local purchase-entitlement data

Local purchase-entitlement records remain on the device until NativeKey app data is cleared or the app is uninstalled.

These records are excluded from NativeKey’s configured Android cloud-backup and device-transfer rules.

Removing local entitlement records does not cancel or refund a Google Play purchase.

Eligible purchases may be restored through Google Play.

Purchase tokens are not stored in the local entitlement record.

### 9.3 On-device AI

NativeKey does not store on-device AI prompts or results on a NativeKey server.

Temporary in-app state may remain in memory or local UI state only as needed to display or apply the current result.

### 9.4 Cloud AI data

For BYOK mode, text sent directly to Google, Anthropic, OpenAI, or another supported provider is handled according to that provider’s policies.

For NativeKey AI, the requested text passes through the NativeKey-operated backend and the configured inference provider. NativeKey does not use the backend as a long-term conversation-history store.

A completed NativeKey AI response may be retained briefly in a short-lived idempotency cache for duplicate-request protection and then expired and purged.

Technical operational records, such as random installation and request identifiers, mode and language metadata, request counts, token counts, model route, latency, status, app version, and timestamps, may be retained for security, quota, reliability, and accounting purposes.

NativeKey does not intentionally store normal keyboard typing as a server-side typing history.

### 9.5 Google Play purchase and subscription data

Google Play retains and processes purchase, payment, account, subscription, and transaction information under Google’s own terms and privacy practices.

For NativeKey AI Pro, NativeKey may retain a server-side entitlement record linked to a random installation identifier. The record may include a SHA-256 hash of the Google Play purchase token, product ID, subscription state, entitlement status, expiry time, and verification timestamps. The raw purchase token is used transiently for Google Play verification or acknowledgement and is not intended to be retained in NativeKey’s database or application logs.

Local NativeKey AI Pro entitlement state remains on the device until app data is cleared or NativeKey is uninstalled. Server-side entitlement metadata may remain as needed for purchase verification, fraud/abuse prevention, entitlement enforcement, operational integrity, and accounting, subject to applicable deletion requirements.

NativeKey does not control Google’s retention periods or Google Play purchase records.

## 10. Accounts and data deletion

NativeKey does not create or require a NativeKey account.

NativeKey does not operate a central user-account database or a server database containing your normal typing content.

You can delete local NativeKey data by:

- clearing learned suggestions in NativeKey settings;
- removing saved API keys;
- clearing NativeKey app storage through Android settings;
- uninstalling NativeKey.

Clearing app data or uninstalling NativeKey removes the local purchase-entitlement records but does not automatically cancel or refund a Google Play purchase.

To manage purchases, refunds, or the Google Play account used for a purchase, use Google Play’s own purchase and account controls.

To request information about deletion of any data that NativeKey may control, contact:

nativekey.support@gmail.com

NativeKey does not maintain a central server-side history of normal typing. If you have used NativeKey AI, limited technical backend records associated with a random installation identifier may exist. Because NativeKey does not require a NativeKey user account, deletion requests may require information that reasonably allows NativeKey to locate the relevant installation records.

For data sent to a cloud AI provider, contact that provider or use its account and privacy controls.

For payment and purchase records held by Google Play, use Google’s account, privacy, payment, and support processes.

## 11. Your choices

You can:

- use NativeKey without cloud AI;
- use on-device AI where supported;
- avoid all AI by not starting an AI action;
- remove saved cloud-provider API keys;
- clear learned suggestions;
- choose whether to purchase either independent one-time product;
- choose whether to subscribe to NativeKey AI Pro;
- manage or cancel an active NativeKey AI Pro subscription through Google Play;
- choose not to start purchase or restore actions;
- disable or switch away from NativeKey in Android system settings;
- clear app data;
- uninstall NativeKey.

## 12. Children

NativeKey is not directed to children under 13 or under the minimum age required by applicable law.

We do not knowingly create NativeKey accounts for children because NativeKey does not provide user accounts.

Purchases are handled through Google Play and may be subject to Google Play family, parental, approval, and payment settings.

## 13. International processing

If you use cloud AI, text may be processed in countries where Google, Anthropic, OpenAI, or NativeKey’s managed infrastructure operate services.

That processing is initiated by your explicit use of a cloud AI action. BYOK requests use the provider and API key you selected; NativeKey AI requests pass through the NativeKey-operated backend to its configured inference provider.

On-device AI processing occurs on the supported Android device, although Android system services may contact Google to prepare or update the model and related system components.

Google Play Billing, payment, and purchase information may be processed in countries where Google and its payment providers operate, under Google’s own terms and privacy practices.

## 14. Changes to this policy

We may update this Privacy Policy when NativeKey’s features, providers, purchase model, data handling, or legal requirements change.

The Last updated date at the top will change when the policy is revised.

For material changes, notice may be provided in the app or on this published page where feasible.

## 15. Contact

Questions or data-deletion requests:

nativekey.support@gmail.com

## 16. Relationship to in-app disclosures

NativeKey includes in-app Privacy & Safety information explaining that:

- normal typing does not call AI;
- local suggestions and learning stay on the device;
- on-device AI processes requests locally on supported devices;
- cloud AI sends text only after an explicit AI action;
- BYOK cloud AI can send the requested text directly to the provider selected by the user;
- NativeKey AI can send the requested text through a NativeKey-operated backend to the configured inference provider and may retain privacy-safe technical metadata plus a short-lived idempotency response cache;
- protected fields disable AI and clipboard reading where designed;
- learned suggestions can be cleared in NativeKey settings;
- optional purchases are handled through Google Play;
- NativeKey does not receive payment-card or bank-account details;
- pending purchases are not recorded as purchased;
- eligible purchases can be restored through a current Google Play query.
