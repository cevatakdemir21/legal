---
layout: legal
permalink: /esign/privacy/
title: Privacy Policy
app_name: eSign
effective: 2026-10-21

# Only the services listed here are described on the page. It matches what the app ships:
#   - documents  : import (Files, Photos, camera scanner, Open In, drop), on-device text
#                  recognition (Vision), Spotlight/Siri index, sharing. No network.
#   - icloud     : CloudKit sync in the user's private database, ON by default
#                  (SettingsStore.syncEnabled); needs silent push (remote-notification).
#   - revenuecat : eSign Pro auto-renewable subscription (weekly, yearly)
#   - posthog    : anonymous product analytics, PostHog EU cloud, no identify, no document
#                  data; on by default, legitimate interest, Settings > Legal > "Analytics"
#                  switch (Analytics.swift, PostHogAnalyticsClient.swift)
#   - sentry     : crash, hang and watchdog reports, Sentry DE region, sendDefaultPii off.
#                  On by default; the SAME "Analytics" switch stops it (CrashReporting.applyAllowed,
#                  called from SettingsStore.analyticsEnabled), hence single_switch below.
#   - storekit   : requestReview after a completed share, and the "Rate us" link
# Keep this in step with the App Privacy label in App Store Connect and with
# eSign/PrivacyInfo.xcprivacy: adding or removing an SDK means updating all three.
services: [documents, icloud, revenuecat, posthog, sentry, storekit]

content_description: "your documents (PDFs, pictures and scans), your signatures and stamps, the items you place on pages, form values, the text recognised on scans, and your settings"

icloud_default_on: true
icloud_silent_push: true
icloud_content: "What syncs: your documents with the items placed on them and their form values, your signatures and stamps and their order, and the Trash. Document names, placed items and form values are stored in CloudKit’s end-to-end encrypted fields, and files are stored as CloudKit assets, which Apple encrypts. Deleting a document, signature or stamp on one device deletes it from your iCloud and from your other devices. A document too large for iCloud stays on the device it is on. Settings such as the theme stay on each device."

analytics_opt_out: true
crash_opt_out: true
single_switch: true

posthog_events_text: "a small set of events that mark steps in using the App: finishing the welcome pages; importing a document (whether it came from Files, Photos, a scan or another app, the kind of file and a rounded page count); creating a signature or stamp (whether it was drawn, typed, made from a photo or a preset); placing a first item; sharing a document (the format, a rounded page count, and how many signatures, stamps, text boxes, dates and marks it held); editing pages, merging documents and using search (the fact that you did, not what you searched for); changing a setting (the setting’s name and its new value); problems such as an error category or a sync problem; and the App being installed, opened, updated or closed. We do not record which screens you view or which controls you tap."
posthog_context_text: "basic technical context: app version, device model, operating system version, a rounded count of the documents in your library, whether iCloud sync is on, and a coarse location (such as country, region or city) derived from your IP address."

sentry_identifier_text: "a random technical identifier that Sentry’s software may generate for the installation, so that repeated reports from one device can be grouped. No name, email address or account identifier is attached to a report, and this identifier is not your Apple Account or your advertising identifier;"
sentry_extra:
  - "a few recent app events leading up to the failure, for example the App moving to the background;"
  - "anonymous session start and end markers, so we can measure how many sessions end in a crash;"
  - "reports of the App freezing or being ended by the system."
---

{% include privacy/body.html %}
