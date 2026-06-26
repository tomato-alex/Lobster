# 🦞 Lobster

## Link Opener - A Simple Tab Session Saver and Restorer

or simply **_Lobster_** (**L**ink **O**pener **B**rowser **S**ave **T**ab **E**xtension **R**evisited)

![Screenshot 1](https://github.com/user-attachments/assets/b375a818-368e-498f-ba99-0c8727dc6fb3) | ![Screenshot 2](https://github.com/user-attachments/assets/b591500b-4569-4615-91e7-760a16d63497)

> _A simple, privacy-friendly tool to save and reopen browser sessions – with tab groups support on Chrome._

---

### ✅ Features

-   Export all open tabs to a `.txt` file
-   Open links from a `.txt` file
-   Export and import **tab groups** via `.json`
-   Dark mode toggle
-   Minimal UI

Created because I have way too many tabs, wanted more control over sessions, and always wanted to build a browser extension.

---

## 🖥️ Why Not Use Built-In Sync Options?

This extension shines in scenarios like:

-   Using **incognito** or privacy-focused browsers
-   Working across devices **without login/sync**
-   Wanting to **save specific tab groups** as named presets
-   Creating **backups** of your browsing sessions
-   Avoiding reliance on `Ctrl/Cmd + Shift + T` or browser restore

---

## 🚧 Current Status

-   ✅ **Chrome:** Fully functional
-   ✅ **Firefox:** Fully functional
    -   Workaround in place due to manifest v3 limitations, utilizing manifest v2 build process for FF.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/tomato-alex/lobster.git
cd lobster/src
```

### 2. Run the build script

```bash
node build.js # For Chrome (default)
node build.js -o firefox # For Firefox
```

> ℹ️ No NPM install or `package.json` needed. This is a simple build script that swaps the manifest file based on the target browser.

### 3. Load the extension

#### 🕶 Chrome

1. Go to `chrome://extensions/`
2. Enable **Developer mode** (top-right)
3. Click **Load unpacked**
4. Select the source folder

> ℹ️ Although the `.crx` file exists, chrome does not allow extensions from outside the webstore to be installed.

#### 🦊 Firefox

1. Go to `about:debugging#/runtime/this-firefox`
2. Click **Load Temporary Add-on...**
3. Select the `manifest.json` from the source folder

> ℹ️ Although a process exists for more permanent extension installation files, I will wait for API Group support in firefox.

---

## 🛠️ Known Issues and Shortcomings

-   Firefox:
    -   Incomplete support for Manifest V3 and `serviceWorker`
-   Manifest differences between Chrome and Firefox require dynamic replacement (`build.js` handles this)

---

## 📋 To-Do

### 🌍 Core Functionality

-   [x] Dark Mode toggle
-   [x] New extension icon
-   [x] Support Chrome and Firefox
-   [x] Export/import tab groups (`.json`)
-   [x] Simplify build script
-   [x] Clean up UI
-   [x] Fix Firefox extension closing when file selection open
-   [ ] Drag & Drop support
-   [ ] Keyboard shortcuts

-   [ ] v1.7 Tab Overview similar to Chrome or Firefox to allow selection of tabs or groups for partial export
-   [ ] v2 Tab Manager for managing tabs (move tabs, etc)
-   [ ] Add shortcuts for moving tab into new window or creating split view
-   [ ] handle split view tabs
-   [ ] open tab in another browser (idk if possible)

### 📦 Packaging

-   [x] Create `.crx` file for easier Chrome installation
-   [x] Create `.zip` for simpler Firefox install
-   [ ] Automate installation files (Chrome and Firefox packaging)

> ℹ️ The Extension is currently undergoing a review in both Chrome Extension store and Firefox Add-on store.

---

## 🧪 Not Yet Possible (Or Practical)

-   **CSV Export:**  
    Technically feasible, but currently disabled. Exporting tab groups in a structured way makes more sense with `.json` for now. If future API changes allow stable group operations across browsers, CSV might be reintroduced.

---

## About

Built for fun, function, and out of a bit of tab-hoarding desperation.
