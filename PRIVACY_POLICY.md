# Felix Debugger – Privacy Policy

**Last updated: April 21, 2026**

## Overview

Felix Debugger is a Chrome DevTools extension that intercepts and displays Google Analytics 4 (GA4) network requests in a human-readable format. It is designed for Digital Analysts and Frontend Developers to debug and validate GA4 implementations.

## Data Collection

Felix Debugger does **not** collect, store, transmit, or share any user data. Specifically:

* **No data is sent to external servers.** The extension operates entirely within your local browser.
* **No personal information is collected.** The extension does not access your name, email, browsing history, or any personally identifiable information.
* **No cookies are set or read.**
* **No analytics or tracking is performed** on users of this extension.
* **Captured GA4 request data is not persisted.** It exists only in memory during your DevTools session and is discarded when the panel is closed.

## Local Storage

Starting with version 4.0, the extension stores a small amount of data persistently on your own device via `chrome.storage.local`. This storage is used exclusively for content you explicitly create inside the extension:

* **Your settings preferences** — the validation profile (GA4 360 or GA4 Basic), and the toggles for Duplicate Event Detection and Semantic E-Commerce Validation.
* **Tracking-plan schemas you import yourself** — the JSON files you drag into the Schema Manager, so they stay available across browser sessions.

This data never leaves your browser. It is not synced to any Google account, not uploaded to any server, and not shared with any third party. You can remove it at any time by uninstalling the extension or by clearing Chrome's extension storage.

## Data Displayed

The extension reads outgoing network requests from your browser to Google Analytics endpoints (analytics.google.com and google-analytics.com). These requests may contain:

* Google Analytics Measurement IDs
* Client IDs and Session IDs
* Event names and custom parameters
* Page URLs and document titles
* Device and browser information
* Consent mode parameters

This data is displayed **only to you** in the DevTools panel. It is never transmitted elsewhere.

## Permissions

The extension requires the following permissions:

* **webRequest**: To intercept outgoing GA4 network requests for display in the DevTools panel. This is read-only; no requests are modified or blocked.
* **host_permissions (<all_urls>)**: Required because GA4 requests originate from the website you are visiting. The webRequest API needs permission for the originating page, not just the destination. The extension only processes requests destined for Google Analytics collect endpoints.
* **storage**: To remember your settings preferences and any tracking-plan schemas you import across browser sessions. This data is stored locally on your device only (see "Local Storage" above).
* **activeTab**: Used only by the browser-action popup to identify the currently active tab so the popup can display the GA4 request summary for that specific tab. The extension does not read the tab's content, URL, or title via this permission.

## Export Feature

The JSON export feature saves data to a local file on your computer. This file is created by you and stored only on your device. The extension does not upload or transmit export files.

## Third-Party Services

Felix Debugger does not integrate with, connect to, or communicate with any third-party services, APIs, or servers.

## Changes to This Policy

If this privacy policy changes, the updated version will be published alongside the extension update.

## Contact

For questions about this privacy policy, contact Felix Kleinknecht.
