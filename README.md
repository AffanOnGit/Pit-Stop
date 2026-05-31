# 🏎️ PitStop

PitStop is a cross-platform mobile application engineered to modernize car maintenance tracking and facilitate a transparent, "trust, but verify" relationship between car owners and local mechanics[cite: 1]. 

Designed with a focus on real-world utility, PitStop eliminates the cumbersome process of manual receipt collection and helps budget-conscious owners and busy professionals manage their vehicle expenses efficiently[cite: 1]. By providing a marketplace of verified local workshops, it democratizes access to high-quality car care outside of expensive dealerships[cite: 1].

## ✨ Core Features

PitStop utilizes a strict role-based architecture, dividing the user experience into two distinct navigation shells upon authentication[cite: 2]:

### For Car Owners
* **Digital Garage:** Add, edit, and manage multiple vehicles within a single account[cite: 1].
* **Maintenance Tracking:** Log service dates, odometer readings, custom descriptions, and categorize them using a color-coded tagging system (e.g., Oil Change, Parts Replacement)[cite: 1].
* **Financial Analytics:** Track maintenance costs over time with interactive visualizations and privacy toggles to hide sensitive cost data[cite: 1].
* **Mechanic Discovery:** Built-in map view utilizing OpenStreetMap tiles to discover nearby mechanics, view their ratings, and read community reviews[cite: 1, 2].
* **Smart Reminders:** Contextual nudges based on time and odometer statistical data to prevent missed maintenance windows[cite: 1].

### For Mechanics & Workshops
* **Public Profiles:** Manage workshop details, address, and service offerings to attract a broader customer base[cite: 1].
* **Reputation Management:** View customer reviews and build a reliable digital reputation[cite: 1].
* **"Founding Mechanic" Program:** Special badging for early adopters who partner with the platform during its initial rollout in localized hubs like H-9[cite: 2].

## 🏗️ System Architecture & Tech Stack

PitStop is designed for high performance, scalability, and offline reliability. 

* **Frontend:** Flutter (Dart) using the Material 3 Design System for a clean, modern, and native "wow" experience across both iOS and Android platforms[cite: 1, 2]. 
* **State Management:** Riverpod for predictable and scalable state transitions[cite: 2].
* **Backend Integration:** Firebase Free Tier ecosystem[cite: 2].
  * **Authentication:** Secure Phone Number/OTP login[cite: 1, 2].
  * **Database:** Cloud Firestore with **Offline Persistence enabled**, ensuring users can log data even in areas with poor mobile connectivity[cite: 2].
  * **Storage:** Firebase Storage for receipt and document uploads[cite: 2].
* **Geolocation & Mapping:** `flutter_map` with OpenStreetMap integration, completely bypassing costly third-party map APIs[cite: 2].

*Note: The initial prototyping and logic validation for this project was developed using React 18, Vite, and Supabase before transitioning to the native Flutter/Firebase architecture.*

## 🔒 Security & Privacy
* **End-to-End Encryption:** User data, including cost of service and personal contact details, is securely stored and encrypted[cite: 1].
* **Role-Based Access Control (RBAC):** Strict isolation between Car Owner, Mechanic, and Super-Admin database access[cite: 2].

## 🚀 Deployment & CI/CD
Beta testing distributions and over-the-air (OTA) updates are handled seamlessly via **Firebase App Distribution**, allowing rapid iteration and feedback loops without the immediate need for Play Store or App Store publishing[cite: 2].
