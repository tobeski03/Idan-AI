# Idan AI

Idan AI is an Android phone assistant built to live close to the device: chat, voice, notifications, Gmail, Google Docs, Google Sheets, WhatsApp workflows, and Shizuku-backed automation.

This public repository is for **APK releases only**. The application source code and server secrets are not published here.

## Download

Get the latest APK from the GitHub Releases page:

https://github.com/tobeski03/Idan-AI/releases

Current release:

https://github.com/tobeski03/Idan-AI/releases/tag/v1.0.0

Download:

```text
idan-release.apk
```

## Android Installation

1. Download `idan-release.apk` from the release page.
2. Open the APK on your Android device.
3. If Android blocks the install, allow installs from your browser or file manager when prompted.
4. Complete the installation.
5. Open **Idan AI**.

If the app was previously installed, install the new APK over the existing one.

## First Launch Setup

Idan needs a few Android capabilities before it can behave like a phone-resident assistant.

### 1. Notification Access

Enable notification access so Idan can observe notifications and prepare replies.

On Android:

```text
Settings -> Notifications -> Device & app notifications -> Notification access
```

Enable Idan AI.

### 2. Microphone Permission

Allow microphone access if you want voice input and conversation mode.

Android will usually ask the first time you use the microphone button.

### 3. Contacts and Call Log

Allow contacts and call-log permissions if you want phone-aware features such as missed-call context, contact lookup, and communication workflows.

### 4. Shizuku

Some device automation features require Shizuku.

Install Shizuku:

https://shizuku.rikka.app/download/

Then:

1. Start Shizuku using your preferred method.
2. Open Idan AI.
3. Grant Idan AI permission when Shizuku asks.

Without Shizuku, chat and cloud-backed features may still work, but deeper Android automation will be limited.

## Google Connection

Model access is tied to a connected Google email.

In the app:

```text
Menu -> Skills -> Google Setup -> Connect Google
```

Sign in with Google and approve the requested scopes.

This enables:

- Server-side model access
- Per-email token allocation
- Gmail support
- Google Docs support
- Google Sheets support

If your Google connection expires, return to **Google Setup** and connect again.

## Token Allocation

Idan uses a backend token allocation system per connected email.

When your email has remaining tokens, model-backed actions can run. When the allocation is exhausted, model activity stops until the allocation is increased on the backend.

This protects the shared AI API key from uncontrolled use.

## Privacy and Security Notes

- The APK does not contain the Gemini API key.
- The APK does not contain the Google OAuth client secret.
- Model requests go through the Idan backend.
- Google OAuth token exchange happens server-side.
- The Android app only stores the connection data needed to use your account features.

Do not install APKs claiming to be Idan AI from unofficial sources.

## Troubleshooting

### Google sign-in fails

Make sure you are using the latest APK from the Releases page.

If the error mentions OAuth redirect URI or client configuration, the backend Google OAuth configuration needs attention.

### Model features do not respond

Check:

1. Google email is connected.
2. Backend is online.
3. Your email still has token allocation.
4. Device has internet access.

### Automation does not work

Check:

1. Shizuku is installed and running.
2. Idan AI is authorized in Shizuku.
3. Required Android permissions are enabled.

### Notification replies do not work

Check:

1. Notification access is enabled.
2. The notification supports inline reply.
3. Idan AI has the needed permissions.

## Release History

### v1.0.0

First public APK release.

Highlights:

- Backend-routed AI model access
- Server-side API key protection
- Google email connection
- Per-email token allocation
- Gmail, Docs, Sheets, notification, voice, and device skills
- Shizuku-backed Android automation support
