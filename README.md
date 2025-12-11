# 📄 Fluxo – Privacy Policy

Last updated: December 11, 2025

Fluxo (“the App”) is a digital sketching and drawing application built with React Native and Expo. Fluxo is designed to operate primarily offline and does not collect or transmit personal data to any server. This Privacy Policy provides clear information about what data Fluxo accesses, stores, or uses.

## 1. Information We Do NOT Collect

Fluxo does not collect, store, transmit, or share any of the following:

- Personal information (name, email, phone number, address, etc.)
- Account or login details
- Location data
- Contacts or calendar data
- Usage analytics or activity tracking
- Device identifiers
- Biometric or sensitive information

Fluxo has no backend servers, no cloud storage, and no analytics SDKs.

## 2. Permissions and Their Purpose

Fluxo uses only the minimal device permissions needed for drawing, saving, and exporting artwork.

### Android Permissions

- **READ_MEDIA_IMAGES / READ_EXTERNAL_STORAGE** — Used only to allow the user to import images into the canvas.
- **WRITE_EXTERNAL_STORAGE (legacy)** — Used only for saving exported sketches into the user's gallery (Fluxo album).
- **INTERNET** — Required by React Native runtime; Fluxo does not communicate with external servers.
- **VIBRATE** — Used for light haptic feedback inside the UI.
- **SYSTEM_ALERT_WINDOW** — Included by the debug/runtime toolchain; not used by the app.
- **RECORD_AUDIO / microphone permissions** — Declared by native templates but not used anywhere in the Fluxo codebase.

Fluxo does not record audio or video.

### iOS Permissions

- **NSPhotoLibraryUsageDescription / AddUsageDescription** — Required for saving sketches into the user’s Photos library.
- **NSCameraUsageDescription / NSMicrophoneUsageDescription** — Declared by the template but not used by the app.

Fluxo does not use the camera or microphone.

## 3. Data Stored Locally on the Device

Fluxo stores all data locally on the user’s device. No data is uploaded or transmitted.

### Sketch Files

Stored under Expo FileSystem:

`FileSystem.documentDirectory/sketches/{id}.json`

Contain:

- Stroke paths
- Colors
- Brush settings
- Background image URI
- Imported images metadata
- Timestamp
- Thumbnail images (PNG base64) stored alongside the JSON.

### User Preferences & Settings

Stored using AsyncStorage:

- Theme selection (light/dark)
- Recent colors used in Color Picker
- Onboarding completion flag
- Launch counter
- Sketch history index (list of sketches) — capped at 5 recent entries

No personal identifiers, accounts, or profile data are stored.

### Exports & Sharing

- Exported sketches are saved as PNGs into the device's Photos gallery (Fluxo album).
- Temporary PNGs are written to `FileSystem.cacheDirectory` when the user shares content.
- Fluxo never uploads or shares these files. The user may choose to share via the system share sheet.

## 4. Network Communication

Fluxo does not send data to any server.

Codex confirmed:

- No fetch, axios, or HTTP requests
- No backend URLs
- No push notifications
- No remote analytics or tracking
- No in-app purchases

The only network-like features are:

- `mailto:` links (for support)
- App store links inside the About screen
- The system share sheet (only user-initiated)

Fluxo never transmits user images, settings, or identifiers automatically.

## 5. Third-Party Services, SDKs, or Data Sharing

Fluxo does not integrate with:

- Analytics (Google Analytics, Firebase, Segment, etc.)
- Crash reporting (Sentry, Bugsnag, etc.)
- Advertising SDKs
- Tracking or profiling tools
- Cloud services
- Social login or identity providers

Fluxo contains zero third-party data sharing.

## 6. Children’s Privacy

Fluxo is suitable for general audiences. The app contains no ads, no social features, and does not collect personal information from children under 13.

## 7. Security

Because Fluxo operates offline and stores all data locally on-device:

- Your sketches never leave your device unless you manually share them.
- No data is transmitted, collected, or processed by Fluxo’s developers.
- Local files remain under the security of your device’s operating system.

## 8. Changes to This Privacy Policy

If Fluxo ever introduces cloud features, accounts, analytics, or additional permissions, this policy will be updated accordingly. Changes will be posted at this same URL.

## 9. Contact Us

For questions or concerns about this policy, contact:

📧 syedabdullah.developer@gmail.com
