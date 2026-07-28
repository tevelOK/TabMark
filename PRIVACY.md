# Privacy Policy for TabMark

**Effective date:** April 2, 2026  

This Privacy Policy describes how the **TabMark** browser extension (“TabMark”, “we”, “us”, or “our”) handles information when you use it. TabMark is built around a **local-first** approach: **your start page data stays under your control** on your device unless you explicitly choose optional features that talk to third-party services.

By using TabMark, you agree to this policy. If you do not agree, please uninstall the extension.

---

## 1. Summary

- We **do not** sell your data, run advertising inside the extension, or use third-party analytics SDKs to track you.
- **Folders, tiles (dials), notes, settings, and usage statistics you see in TabMark** are stored **locally** in your browser (see §2).
- **Browsing history, installed extensions list, and similar browser APIs** are used **only** to show you information in the UI (e.g. search/history menus); TabMark **does not** send that content to our servers—we **do not operate** a backend that receives your browsing data.
- **Optional Google Drive backup** uploads a file **you** initiate **to your own Google account**, using Google’s APIs (see §4).
- **Optional weather** may call weather and location-related endpoints over the network (see §5).

---

## 2. Data stored locally on your device

TabMark stores and reads data using browser extension storage (including `chrome.storage` with expanded quota where the browser allows) and other **local** mechanisms the extension is permitted to use. Typical categories include:

| Category | Examples | Notes |
|----------|----------|--------|
| **Tiles and folders** | Names, URLs, order, folder colors/icons | Stays on your device. |
| **Appearance & layout** | Grid options, backgrounds, fonts, toggles | Stays on your device. |
| **Notes** | Text you enter in the notes panel | Stays on your device. |
| **In-extension statistics** | e.g. click counts / stats shown in the UI | Processed and stored locally for your dashboard. |

This data is **not** transmitted to TabMark’s servers, because **we do not operate** collection servers for that purpose.

---

## 3. Permissions and what they are for

TabMark requests only what it needs for documented features. In the current manifest, that includes:

| Permission | Purpose |
|----------|---------|
| **`storage` / `unlimitedStorage`** | Persist tiles, folders, settings, and related data locally. |
| **`bookmarks`** | Integrate with browser bookmarks where the feature needs it (e.g. unified search / bookmark-related actions). |
| **`tabs`** | Work with open tabs (e.g. collecting tabs into a folder, new-tab behaviour). |
| **`history`** | Read history **to power in-UI search/history features**; not uploaded to us. |
| **`search`** | Integrate with the browser’s search capabilities where implemented. |
| **`management`** | List installed extensions **only** to power the “Apps” / extensions panel in the UI. |
| **`contextMenus`** | Add “Add to TabMark” (or equivalent) in the context menu. |
| **`identity`** | **Optional** sign-in to Google **when you enable** Google Drive backup/sync. |
| **`alarms`** | Schedule **local** background tasks (e.g. sync checks you configure). |
| **`geolocation`** | **Optional** coarse location for the **weather widget**, if you use it and the browser prompts you. |

If you do not use a feature, the related permission may still be declared in the manifest, but **network or sensitive use** is limited to what that feature requires (e.g. Drive only after you connect Google).

---

## 4. Optional Google Drive backup / sync

If you choose to connect **Google Drive**:

- Authentication uses Google’s **OAuth 2.0** with the scope required for **creating/accessing app-specific files** on **your** Drive (as declared in the extension manifest, e.g. `https://www.googleapis.com/auth/drive.file`).
- A **backup** is prepared **when you use the sync/backup actions**—not silently sent to us. Before upload, the extension **encrypts** that payload (so the raw JSON of your tiles/settings is not stored on Drive in plain text).
- The backup file resides in **your** Google account; **Google’s privacy policy** also applies to data stored on Google Drive.

We do **not** receive a copy of your Drive backup on our own infrastructure.

---

## 5. Network requests and third-party services

TabMark may make **outbound HTTPS requests** for the following reasons:

1. **Weather widget** (if enabled):  
   - **`api.openweathermap.org`** — if you provide an API key for OpenWeatherMap.  
   - **`wttr.in`** — optional weather source without a key (as configured in the extension).  
   - **`ipapi.co`** — may be used for location-related hints when resolving weather (as allowed in the extension’s content security policy).

2. **Google APIs** (`https://www.googleapis.com`):  
   - Used for **optional** Google sign-in / Drive operations **when you enable them**.

3. **Favicons / site icons**:  
   - The browser or common favicon resolution mechanisms may request icons from third parties (e.g. Google’s public favicon service or the site itself). These requests are **not** used to build a personal profile for us; we do not operate that infrastructure.

4. **Fonts (UI)**:  
   - The extension may load fonts from **Google Fonts** (`fonts.googleapis.com` / `fonts.gstatic.com`) as permitted by its content security policy.

We do **not** embed third-party **advertising** or **analytics** trackers whose purpose is to profile you across the web.

---

## 6. Import and export

**Export** lets you save a **`.json`** (or similar) file with your TabMark configuration to **your computer**.  
**Import** lets you load such a file **from your computer** into the extension.

Those operations run **inside your browser**. The file is **yours**; we do not receive it unless you separately send it to us (e.g. by email for support).

---

## 7. Children’s privacy

TabMark is not directed at children under 13 (or the minimum age required in your jurisdiction). We do not knowingly collect personal information from children.

---

## 8. Changes to this policy

We may update this Privacy Policy from time to time. The **Effective date** at the top will change when we do. Continued use after changes means you accept the updated policy. For material changes, we encourage you to review this page when you update the extension.

---

## 9. Open source and contact

TabMark may be distributed as open source (e.g. on GitHub). The **published source** and **manifest** are the most precise reference for what the build can do; this policy is meant to explain it in plain language.

**Questions about this Privacy Policy:**  
**[tevelok@vk.com](mailto:tevelok@vk.com)**

---

*This document is provided for informational purposes and does not constitute legal advice.*
