# NativeKey Privacy Policy

**Last updated: 2026-07-27**

**Contact:** nativekey.support@gmail.com

This Privacy Policy explains how NativeKey, an Android custom keyboard app published under the package name `com.nativekey.keyboard`, handles information when you use the app.

NativeKey is a keyboard input method. It lets you type into other apps, provides optional on-device suggestions and learning, and offers optional AI-assisted writing, rewriting, translation, and understanding features.

## Summary

- Normal typing is processed on your device and sent only to the app you are typing into, also called the host app.
- Normal typing does not call an AI service.
- Local suggestions and learned words stay on your device.
- On supported devices, NativeKey can use on-device AI powered by Gemini Nano through Android system services. In this mode, the prompt and result are processed on the device and are not sent to a cloud AI provider for inference.
- Cloud AI features run only when you explicitly request them. Depending on your selected provider, text may be sent over HTTPS to Google Gemini, Anthropic Claude, or OpenAI using your own API key.
- Clipboard text is used for incoming translation or similar AI flows only when you start that flow.
- Protected contexts such as passwords, banking apps, and similar sensitive fields disable AI, clipboard-based AI flows, suggestions, and local learning where designed.
- NativeKey does not include advertising SDKs or third-party analytics SDKs.
- NativeKey does not sell personal data.
- NativeKey does not create or require a NativeKey user account.
- NativeKey does not operate a central database of your typing content.

This policy does not claim that no data ever leaves your device. Text can leave the device when you explicitly use a cloud AI provider.

## 1. What NativeKey is

NativeKey is a third-party Android keyboard. When enabled in Android system settings, it can:

- insert characters into text fields in other apps;
- show optional local word suggestions;
- optionally learn frequently used words, correction choices, and word pairs on your device;
- optionally help you write, rewrite, translate, or understand text;
- use either supported on-device AI or a cloud AI provider that you configure.

Android displays a standard warning when any third-party keyboard is enabled. NativeKey is designed so that normal typing does not call AI services and protected fields use a privacy-safe keyboard mode.

## 2. Information processed locally on your device

### 2.1 Normal typing

When you type without using AI:

- keystrokes are handled on your device to display the keyboard and commit text to the active field in the host app;
- this typing flow does not send your text to NativeKey-operated servers;
- normal typing does not call Gemini, Claude, OpenAI, or another cloud AI API.

### 2.2 Local suggestions

NativeKey can suggest words from built-in word lists and from on-device learning. Suggestion generation and ranking are performed locally.

Local suggestions are not sent to cloud AI providers for ranking.

### 2.3 Local learning

When enabled and allowed for the current field, NativeKey may store local statistics such as learned words, correction choices, and word-pair patterns to improve future suggestions.

This information remains in app-private storage on your device.

You can delete learned suggestion data in:

**Settings → Privacy & Safety → Local suggestions → Clear learned suggestions**

This control removes locally learned suggestion data. It does not remove API keys, keyboard language choices, AI settings, or Keyboard Lab customization.

### 2.4 Settings and preferences

NativeKey stores settings locally, including:

- keyboard layouts and enabled languages;
- typing and feedback preferences;
- AI language and provider settings;
- Keyboard Lab customization;
- other app preferences required to provide the selected behavior.

### 2.5 On-device AI

On supported devices, NativeKey can use Gemini Nano through Android's on-device AI system services and ML Kit GenAI APIs.

When on-device AI is selected:

- the prompt and result are processed on the device;
- NativeKey does not send that prompt to Google Gemini cloud, Anthropic, or OpenAI for inference;
- an API key is not required for the on-device request;
- availability depends on the device, Android system components, model readiness, and supported languages or capabilities.

Android or Google system services may download, update, prepare, or manage the on-device model and related components. Those system services are controlled by Google and Android and may handle technical service information under their own terms. NativeKey does not receive your prompt through a NativeKey server.

### 2.6 Privacy-safe and protected contexts

To reduce exposure of sensitive information, NativeKey checks local field metadata and app context, such as input type flags, field hints, package names, and app labels.

This detection is performed locally and does not upload your typed content for classification.

In protected contexts, NativeKey is intended to operate as a normal keyboard only. AI actions, clipboard reading for AI, local suggestions, local learning, and related features are disabled where designed.

## 3. Information that may leave your device

### 3.1 Cloud AI features

Cloud AI features are optional.

If you save an API key and explicitly start a cloud AI action, NativeKey may send the following over HTTPS:

- selected text;
- text you typed;
- copied clipboard text used for an incoming AI flow;
- source and target language choices;
- instructions needed to complete the requested AI action.

The data is sent to the provider you selected under:

**Settings → Connect your AI**

Supported cloud providers may include:

- Google Gemini;
- Anthropic Claude;
- OpenAI.

Cloud AI requests use your own API key. NativeKey does not provide a shared AI service account on your behalf.

Outgoing AI actions, such as rewriting or translating text you wrote, run only after you explicitly request the action.

Incoming AI actions, such as translating copied text, may read clipboard plain text only after you initiate the incoming AI flow.

If you do not configure a cloud provider or do not start a cloud AI action, cloud AI transmission does not occur.

### 3.2 Third-party AI providers

When text is sent to Google, Anthropic, or OpenAI, that provider processes it under its own terms, privacy policy, account settings, and retention rules.

NativeKey does not operate those services and cannot guarantee:

- how long a provider retains a request;
- whether a provider uses request data for service improvement;
- which account-level privacy controls are available;
- whether NativeKey can delete data from that provider's systems.

For requests concerning data held by a cloud AI provider, use that provider's account, privacy, and support processes.

## 4. API keys

Cloud AI features require an API key obtained directly from the selected provider.

- API keys are stored locally in encrypted app-private storage using Android security APIs.
- Saved keys are hidden in the NativeKey interface.
- NativeKey does not intentionally send your API key to a NativeKey-operated server.
- A key is sent only to the selected provider as required for an HTTPS AI request.
- You can remove saved keys under **Settings → Connect your AI**.
- Removing a key stops future NativeKey requests to that provider unless a new key is saved.

Treat API keys like passwords. You are responsible for use, limits, and billing associated with your provider account.

NativeKey excludes certain preference files, including files that may contain API keys and learned suggestion data, from the Android cloud-backup rules configured by the app. You should nevertheless assume that a saved key remains on the device until you remove it, clear app data, or uninstall NativeKey.

## 5. Clipboard

NativeKey may read clipboard plain text when:

- you start an incoming AI or translation flow that relies on copied text; and
- the current field is not a protected context where clipboard-based AI is disabled.

NativeKey does not declare a separate Android clipboard permission. Clipboard access uses Android platform APIs available to the keyboard in the relevant context.

Clipboard text used with on-device AI is processed on the device.

Clipboard text used with a cloud AI action may be sent to the selected provider as described in Section 3.

NativeKey does not send clipboard text to an AI provider in the background without your action.

## 6. Permissions and Android access

NativeKey declares the `INTERNET` permission so it can contact a cloud AI provider when you explicitly use a cloud AI feature.

The NativeKey input-method service is protected by Android's `BIND_INPUT_METHOD` system permission. This allows NativeKey to function as a keyboard and is controlled by Android.

NativeKey does not request permissions for:

- contacts;
- location;
- camera;
- microphone;
- SMS;
- call logs;
- broad external storage access.

## 7. Analytics, advertising, and sale of data

Based on the current app implementation:

- NativeKey does not integrate third-party analytics SDKs;
- NativeKey does not integrate advertising SDKs;
- NativeKey does not sell personal data.

If this changes in a future version, this policy and the Google Play Data Safety declaration will be updated before or alongside that release.

## 8. Data retention

### 8.1 Local data

Learned words, correction choices, and word-pair patterns remain on your device until you:

- clear learned suggestions in NativeKey;
- clear NativeKey app data;
- uninstall NativeKey.

Saved API keys remain on your device until you:

- remove them in NativeKey settings;
- clear NativeKey app data;
- uninstall NativeKey.

Other local settings remain until changed, cleared, or removed with the app.

### 8.2 On-device AI

NativeKey does not store on-device AI prompts or results on a NativeKey server.

Temporary in-app state may remain in memory or local UI state only as needed to display or apply the current result.

### 8.3 Cloud AI data

Text sent to Google, Anthropic, or OpenAI is handled according to the selected provider's policies.

NativeKey does not control the provider's retention period and cannot delete provider-held request data on your behalf.

## 9. Accounts and data deletion

NativeKey does not create or require a NativeKey account.

NativeKey does not operate a central user-account database or a server database containing your normal typing content.

You can delete local NativeKey data by:

- clearing learned suggestions in NativeKey settings;
- removing saved API keys;
- clearing NativeKey app storage through Android settings;
- uninstalling NativeKey.

To request information about deletion of any data that NativeKey may control, contact:

**nativekey.support@gmail.com**

Because NativeKey does not maintain user accounts or a central database of typing content, there may be no server-side NativeKey data associated with your request.

For data sent to a cloud AI provider, contact that provider or use its account and privacy controls.

## 10. Your choices

You can:

- use NativeKey without cloud AI;
- use on-device AI where supported;
- avoid all AI by not starting an AI action;
- remove saved cloud-provider API keys;
- clear learned suggestions;
- disable or switch away from NativeKey in Android system settings;
- clear app data;
- uninstall NativeKey.

## 11. Children

NativeKey is not directed to children under 13 or under the minimum age required by applicable law.

We do not knowingly create NativeKey accounts for children because NativeKey does not provide user accounts.

## 12. International processing

If you use cloud AI, text may be processed in countries where Google, Anthropic, or OpenAI operate infrastructure.

That processing is initiated by your explicit use of the selected cloud AI provider with your own API key.

On-device AI processing occurs on the supported Android device, although Android system services may contact Google to prepare or update the model and related system components.

## 13. Changes to this policy

We may update this Privacy Policy when NativeKey's features, providers, data handling, or legal requirements change.

The **Last updated** date at the top will change when the policy is revised.

For material changes, notice may be provided in the app or on this published page where feasible.

## 14. Contact

Questions or data-deletion requests:

**nativekey.support@gmail.com**

## 15. Relationship to in-app disclosures

NativeKey includes in-app Privacy & Safety information explaining that:

- normal typing does not call AI;
- local suggestions and learning stay on the device;
- on-device AI processes requests locally on supported devices;
- cloud AI sends text only after an explicit AI action;
- protected fields disable AI and clipboard reading where designed;
- learned suggestions can be cleared in NativeKey settings.
