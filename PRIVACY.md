# Privacy Policy for TabMark

**Effective Date:** November 5, 2025

This Privacy Policy describes how the "TabMark" browser extension ("we," "us," or "our") handles your data. Our core philosophy is simple: **your data is yours**. We do not collect, store, or transmit any of your personal information.

## 1. Data We Handle (And How)

TabMark is designed to be a local-first application. All data it accesses or creates stays on your computer.

### User-Created Data (Locally Stored)

* **Folders and Dials:** All folders, links (URLs), names, and custom settings (colors, background images) you create are saved using the `chrome.storage.local` API.
* **Extension Settings:** Your preferences, such as grid layout, background settings, and UI toggles, are saved in your browser's `localStorage`.
* **This data is stored *only* on your local machine.** It is never sent to or stored on any external server.

### Browser Data (Locally Accessed)

* **Browsing History (`history` permission):** We request the `history` permission solely to power the "History" (📚) dropdown menu. This data is read from your browser, displayed to you in that menu, and is *never* stored, analyzed, or transmitted by us.
* **Installed Apps (`management` permission):** We request the `management` permission solely to power the "Apps" (🎛️) dropdown menu. This data is read from your browser, displayed to you in that menu, and is *never* stored, analyzed, or transmitted by us.

## 2. Import and Export Feature

TabMark provides an "Import/Export" feature for your convenience.

* **Export:** This feature allows *you* to save a file (`.json`) containing your local TabMark settings (folders, dials, etc.) directly to your computer. This file is for your own backup or transfer purposes.
* **Import:** This feature allows *you* to upload a previously exported settings file from your computer to restore your configuration.

At no point during the export or import process is this data sent to us or any third party. The entire operation occurs locally within your browser.

## 3. Third-Parties

We do not use any third-party analytics, advertising, or data collection services. We do not share any data with third parties because we do not collect any data to begin with.

The only external requests made by the extension are:
* To fetch favicons for the websites you add (using a public Google favicon service). This is an anonymous request to Google's servers to display an icon and does not involve your personal data.

## 4. Changes to This Policy

We may update this Privacy Policy in the future. Any changes will be posted on this page, and we will update the "Effective Date" at the top. We encourage you to review this policy periodically.

## 5. Contact Us

If you have any questions about this Privacy Policy, please contact us at:
**[tevelok@bk.ru](mailto:tevelok@bk.ru)**