# Privacy Policy for Causali

**Last Updated:** November 12, 2026  
**Effective Date:** November 12, 2026  

**Causali** is an offline food and symptom diary application for Android, developed by **Hugo EYNARD** (independent developer).

---

## Quick Summary

- **100% Offline:** Causali has no remote servers, no cloud databases, and no user accounts.
- **Zero Data Collection:** Your food, symptom, and health entries never leave your device unless you yourself export a backup or share a recipe or custom food. The developer cannot view, access, or recover your data.
- **Full Privacy & Security:** Your data is encrypted at rest, excluded from unencrypted cloud backups, and under your complete control.

---

## 1. 100% Offline Architecture

- **No Remote Servers:** Causali does not communicate with external servers or cloud services.
- **No Internet Access:** Causali does not request or possess Android network permissions (INTERNET or ACCESS_NETWORK_STATE). The Android operating system therefore prevents the application from sending data over the network.
- **No Third-Party Tracking:** Causali contains zero advertising SDKs, zero analytics trackers, and zero remote crash reporting services. Background telemetry components bundled transitively by on-device libraries are disabled in the application manifest.

---

## 2. Information Handled on Your Device

All information you record is stored locally in the application's private sandbox on your device:

- **Meals & Nutrition:** Meal names, timestamps, portion weights in grams, nutritional values (calories, macros, micros), FODMAP classifications, and custom foods or recipes you create.
- **Symptoms & Health:** Symptoms you choose to track (such as bloating, abdominal pain, cramps, nausea, diarrhea, constipation, headache, or fatigue), severity ratings (Mild, Moderate, Severe), and timestamps.
- **Goals & Preferences:** Daily calorie, macronutrient, and micronutrient targets, default meal schedules, food presets, the app language, and display settings.
- **Correlations:** Statistical calculations (Relative Risk, 95% Confidence Intervals, Phi coefficient, and p-values) computed on-device to help you discover associations between foods and symptoms.

---

## 3. Device Permissions

### Camera (Optional)
- **Purpose:** Used solely to scan retail grocery barcodes (EAN-13, EAN-8, UPC-A, UPC-E) against the offline food database, and to scan Causali QR codes when you import a recipe or custom food shared by another user.
- **Real-Time Memory Processing:** Camera frames are analyzed temporarily in device memory (RAM) via Google ML Kit and released immediately after analysis.
- **No Photos or Video:** Causali never captures, saves, records, or transmits photos or video frames.
- **Optional Access:** You can decline or revoke camera permission at any time and search or enter foods and barcodes manually.

---

## 4. Local Security & Storage

- **Database Encryption:** Your diary database (meals, foods, recipes, and symptoms) is encrypted at rest using SQLCipher (AES-256).
- **Settings Encryption:** Default meal presets and nutrition goals stored in application settings are encrypted at rest using AES-256-GCM. Simple display preferences (meal period names, on/off options, and the app language) are stored unencrypted in the application's private storage.
- **Hardware-Backed Keys:** Encryption keys are generated and protected by the Android KeyStore using hardware-backed isolation (TEE or StrongBox) when available on your device.
- **Cloud Backup Exclusion:** Android Auto Backup and device-to-device migration rules are configured to exclude your diary database, settings, and encryption keys from being uploaded to Google Drive or transferred unencrypted.

---

## 5. Your Data Control & Deletion

- **Exporting Data:** You can export your full diary, custom foods, recipes, and settings at any time as an unencrypted JSON file or a password-protected AES-256 encrypted ZIP archive using Android's system file picker. Once exported, you are responsible for safeguarding the file in your chosen location.
- **Importing Data:** You can restore or merge previous backups from files stored on your device.
- **Sharing by QR Code:** You can choose to display a QR code for one of your recipes or custom foods so that another Causali user can scan it. The code contains only that recipe or food (name, ingredients, quantities, and nutrition and FODMAP values). It never contains your diary, symptoms, goals, or anything identifying you. Nothing is sent over a network; the code only exists on your screen, and anyone who can see or photograph it can read its contents.
- **Deleting Records:** You can edit or delete individual entries directly within the diary at any time.
- **Erasing All Data:** You can permanently delete all local data and cryptographic keys by clearing the app's storage in Android Settings or by uninstalling Causali. Because no data exists on external servers, local deletion is complete and irreversible.

---

## 6. International Privacy Rights & Disclosures

### European Economic Area & UK (GDPR / UK GDPR)
- **No Processing by the Developer:** Hugo EYNARD is the developer of Causali. Because the application operates offline and transmits no data, the developer does not collect, receive, store, or otherwise process your personal information, and cannot act on requests concerning data that exists only on your device.
- **Health Data:** Health and dietary entries are data concerning health. You decide what to enter; it is processed only on your device, under your sole control, for your personal use.
- **Access, Correction, Erasure, and Portability:** You can view, correct, delete, and export all of your data directly at any time using the in-app view, edit, delete, and export features.

### California (CCPA / CPRA)
- The developer does not collect, sell, rent, or share personal or sensitive personal information, and Causali does not engage in cross-context behavioral tracking.

---

## 7. Children's Privacy

Causali is not directed to individuals under 13 years of age (or under 16 in the EEA/UK) and does not collect personal information from anyone.

---

## 8. Medical & Health Disclaimer

**Causali is not a medical device and does not provide medical diagnoses, clinical advice, or treatment plans.**  
Nutritional data, FODMAP classifications, and statistical correlations are provided solely for personal tracking and informational purposes. Always consult a qualified physician, gastroenterologist, or registered dietitian before making medical decisions or beginning an elimination diet.

---

## 9. Changes to This Privacy Policy

Any revisions to this Privacy Policy will be published at https://hugogo22.github.io/causali-privacy-policy/en/ and summarized in the application's release notes.

---

## 10. Contact

For questions or feedback regarding this Privacy Policy, please contact:

- **Developer:** Hugo EYNARD  
- **Email:** hugo.eynard.dev@gmail.com  
