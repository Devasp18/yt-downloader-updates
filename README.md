# 🔄 YT Downloader – Update Server

This repository acts as the **update metadata server** for the
**YT Video Downloader** desktop application.

It hosts the `latest.json` file which is periodically checked by the app
to determine whether a newer version is available.

---

## 📌 Purpose

* Provide update information to the desktop application
* Enable seamless in-app update notifications
* Decouple update logic from the main source code repository

This repository **does NOT contain application source code or installers**.

---

## 📁 Repository Structure

```
yt-downloader-updates/
 ├── latest.json   # Update metadata consumed by the app
 └── README.md
```

---

## 📄 latest.json

The `latest.json` file contains:

* Latest application version
* Release date
* Download URL (MSI installer hosted in main repo releases)
* Changelog
* Minimum supported version
* Mandatory update flag

The application fetches update data from:

```
https://raw.githubusercontent.com/Devasp18/yt-downloader-updates/main/latest.json
```

---

## 🔁 Update Flow

1. Application starts
2. App fetches `latest.json`
3. Local version is compared with remote version
4. If a newer version exists:

   * User is notified
   * Installer is downloaded
   * Update proceeds after user confirmation

---

## 🚫 Important Notes

* This repository is **not intended for end users**
* Do **not** upload installers here
* Only update `latest.json` when publishing a new app release

---

## 🔗 Main Application Repository

👉 **YT Video Downloader**
[https://github.com/Devasp18/YT_Downloader](https://github.com/Devasp18/YT_Downloader)

---

## 👨‍💻 Maintainer

**Devasp18**
