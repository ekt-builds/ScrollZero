# ScrollZero

**ScrollZero** is a lightweight, 100% offline Android application built with Kotlin and Jetpack Compose that automatically exits short-form video feeds (**YouTube Shorts**, **Instagram Reels**, **Facebook Reels**, and **TikTok**) while leaving standard videos, messages, and posts untouched.

- **100% Offline & Private:** Zero internet permissions, zero analytics, and zero external servers.
- **Persistent Foreground Shield:** Uses a silent `specialUse` foreground service with a master pause/resume toggle so the blocker stays active in the background.
- **Multi-Brand Persistence Guide:** Automatically detects Xiaomi/HyperOS, Samsung One UI, Oppo/Realme/OnePlus, Vivo/iQOO, or Stock Android and displays tailored background-lock instructions.

---

## Download

Grab the latest signed `app-release.apk` from the **[Releases](../../releases)** page on the right sidebar.

---

## Installation & Google Play Protect Guide

Because ScrollZero uses Android's `AccessibilityService` API and is distributed directly via APK outside the Google Play Store, Android's security protections require two quick one-time steps when installing:

### Step 1: Bypass the Google Play Protect Warning
When tapping `app-release.apk`, Google Play Protect may show **"Blocked by Play Protect"** or **"Unsafe app blocked"** because the APK is signed with an independent developer key:

* **Method 1 (Quickest):** On the Play Protect dialog, tap **More details** → **Install anyway**.
* **Method 2 (If "Install anyway" is hidden on Xiaomi / HyperOS / Android 15+):**
  1. Open the **Google Play Store** → tap your **Profile icon** (top-right) → **Play Protect** → tap the **Gear icon** (top-right).
  2. Temporarily turn **OFF** **Scan apps with Play Protect**.
  3. Install `app-release.apk` from your File Manager.
  4. Return to Play Protect settings and turn **Scan apps with Play Protect** back **ON**.
* **Method 3 (USB / ADB):** Installing from a PC via `adb install app-release.apk` skips both Play Protect and Restricted Settings automatically.

### Step 2: Unlock "Controlled by Restricted Setting" (Android 13+)
Android blocks sideloaded APKs from enabling Accessibility Services until you explicitly grant restricted access:

1. Open **ScrollZero** and tap **Open Accessibility Settings**.
2. Tap **Downloaded apps** (or **Installed services**) → tap **ScrollZero** (it will appear greyed out or say *"Controlled by Restricted Setting"*).
3. Open your phone's **Settings → Apps → ScrollZero** (or tap **Open ScrollZero App Info** inside the app).
4. Tap the **⋮ (More)** menu in the top-right or bottom corner (or **Other permissions** on HyperOS) and select **Allow restricted settings**.
5. Return to **Accessibility** and toggle **ScrollZero** **ON**.

### Step 3: Keep ScrollZero Running 24/7
Open **ScrollZero**, tap **Allow Unrestricted Background**, and complete the device-specific checklist at the bottom of the screen (enabling **Autostart**, setting Battery to **No restrictions / Unrestricted**, turning **OFF** *Pause app activity if unused*, and locking the app in **Recent Apps**).
