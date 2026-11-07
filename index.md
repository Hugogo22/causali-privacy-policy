# Privacy Policy for Causali

**Last Updated:** November 7, 2026  
**Effective Date:** November 7, 2026  

Welcome to **Causali** (the "Application"), developed by **Hugo EYNARD** ("we", "our", or "us"). 

We believe that your personal health, dietary habits, and digestive symptoms are among the most sensitive personal data you possess. Causali is engineered from the ground up on the principle of **Privacy by Design**: an offline-first architecture where your data belongs exclusively to you and never leaves your physical device.

---

## 1. Core Architecture: 100% Offline by Design

- **Zero Remote Servers:** We do not operate remote servers, cloud databases, user registration systems, or backend sync infrastructure.
- **No Internet Access:** Causali does not request or possess the Android `android.permission.INTERNET` or `android.permission.ACCESS_NETWORK_STATE` permissions. The application cannot communicate over the internet, make HTTP/HTTPS network calls, or transmit any data off your device.
- **Zero Third-Party Tracking & Telemetry:** We do not bundle third-party analytics (e.g., Google Analytics, Firebase), advertising SDKs, tracking frameworks, or remote crash reporting services. All diagnostic telemetry pipelines in bundled libraries have been stripped at the operating system manifest level.

---

## 2. Information Handled by the Application

All information you record in Causali is processed, analyzed, and stored strictly locally on your physical device:

### A. Dietary & Nutrition Data
- Food intake logs, meal names, and meal timestamps.
- Serving quantities (in grams) and ingredient breakdowns.
- Nutritional values (calories, macronutrients, and micronutrients).
- Custom food items, recipes, and barcode associations created by you.

### B. Health & Symptom Data
- Gastrointestinal and physical symptoms (e.g., bloating, abdominal cramps, pain, nausea, diarrhea, constipation, headache, fatigue).
- Symptom severity ratings (`MILD`, `MODERATE`, `SEVERE`).
- Date and time of symptom occurrences.

### C. On-Device Statistical Analysis
- Causali calculates statistical correlations (Relative Risk, 95% Confidence Intervals, Phi coefficient, and Fisher's exact test p-values) entirely on your device's processor to help you discover relationships between your diet and symptoms.

---

## 3. Device Permissions & Camera Usage

Causali requests only the minimum necessary hardware permissions:

### Camera Permission (`android.permission.CAMERA`)
- **Purpose:** Used solely for scanning retail product barcodes (EAN-13, EAN-8, UPC-A, UPC-E) to match packaged grocery products against our local offline food database.
- **On-Device Ephemeral Processing:** Camera video frames are analyzed in temporary device memory (RAM) using on-device ML Kit barcode recognition.
- **Zero Storage or Transmission:** The application **never** captures, photographs, records, saves, or transmits images or video feeds. Once a barcode is decoded or the scanner is closed, camera buffers are immediately freed.
- **Strictly Optional:** Camera access is entirely optional. You may decline this permission and search or enter foods and barcodes manually without restriction.

---

## 4. Data Storage & Security Safeguards

We protect your information with defense-in-depth security:

- **AES-256 Database Encryption at Rest:** Your local database is encrypted using SQLCipher with 256-bit AES encryption.
- **Hardware-Backed Master Key:** Cryptographic keys are generated and securely stored in the **Android KeyStore** using hardware-backed isolation (TEE / StrongBox) where supported by your device.
- **Exclusion from OS Cloud Backups:** We have explicitly configured Android backup rules (`backup_rules.xml` and `data_extraction_rules.xml`) to prevent your diary database and security keys from being uploaded to unencrypted Google Drive cloud backups or device-to-device transfers.

---

## 5. User Control, Portability & Data Deletion

You retain complete ownership and control over your data:

- **Data Export:** You can export your full diary, custom foods, recipes, and settings at any time in plain JSON format or as a password-protected, AES-256 encrypted ZIP archive.
- **Data Import:** You can restore or merge your own exported backups at any time.
- **Permanent Deletion:**
  - You can delete individual meal or symptom records directly within the diary.
  - You can permanently and irreversibly destroy all local records and encryption keys at any time by selecting **Clear Data / Clear Storage** in your Android device's app settings, or by uninstalling the application. Because no copies exist on remote servers, deletion from your device is complete and permanent.

---

## 6. International Compliance & Rights

### European Union & UK (GDPR / UK GDPR)
- **Special Category Data (Article 9):** Causali processes health-related data solely based on your explicit consent, which you give by deliberately logging entries into your personal diary.
- **Data Subject Rights:** Your rights to Access, Rectification, Erasure, and Data Portability are directly executable by you at any time using the in-app editing, deletion, and backup export features.

### California (CCPA / CPRA)
- We do not sell, rent, or share personal information or sensitive personal information.
- We do not track consumers across third-party applications or websites.

---

## 7. Children's Privacy

Causali is not directed to individuals under 13 years of age (or under 16 in the EEA/UK). We do not knowingly collect personal information from children.

---

## 8. Medical & Health Disclaimer

**Causali is not a medical device (SaMD) and does not provide medical diagnoses, clinical advice, or treatment plans.**  
The statistical correlations and nutritional values provided by the application are for personal tracking and informational purposes only. Always consult a qualified physician, gastroenterologist, or registered dietitian before making significant changes to your medical treatment or diet.

---

## 9. Changes to This Privacy Policy

If we update this Privacy Policy, the revised version will be published at this repository URL and noted in the application's release notes.

---

## 10. Contact Us

If you have questions or feedback regarding this Privacy Policy, please contact:

- **Developer:** Hugo EYNARD  
- **Email:** hugo.eynard@gmail.com  
- **Repository:** [https://github.com/Hugogo22/causali-privacy-policy](https://github.com/Hugogo22/causali-privacy-policy)  
