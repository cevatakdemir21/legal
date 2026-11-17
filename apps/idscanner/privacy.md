---
layout: legal
permalink: /idscanner/privacy/
title: Privacy Policy
app_name: ID Scanner
effective: 2026-11-17

# What the app actually ships (checked against the code on 17 Nov 2026):
#   - idscan     : camera reads PDF417 barcodes and passport MRZ lines on device; saved fields
#                  (incl. date of birth and issue date since 12 Nov), never-saved fields, salted
#                  SHA-256 code, VIP/Banned lists and notes, fixed 90-day retention (no setting,
#                  no Save History switch), deleting scans by period in History, CSV export,
#                  Contact Support / Request a Feature email drafts
#   - icloud     : SwiftData + CloudKit private database, OFF by default (Settings > General >
#                  iCloud Sync); scans, VIP/Banned lists and a few settings; the salt goes
#                  through iCloud Keychain while it is on
#   - revenuecat : "Unlimited" auto-renewable subscription (weekly, yearly); 10 free scans a day,
#                  counted in the device's Keychain only
#   - posthog    : anonymous product analytics, PostHog EU cloud, no identify, no person profile,
#                  no scanned-ID data; scans go as one daily summary of counts (scans_daily);
#                  every event carries $geoip_disable; on by default, legitimate interest,
#                  Settings > About Us > "Analytics" (Core/Analytics/Analytics.swift)
#   - sentry     : crashes, fully blocking hangs, watchdog terminations, MetricKit diagnostics,
#                  session health and sampled performance traces (app start, screen loads,
#                  slow/frozen frames); Sentry DE region; sendDefaultPii off, no screenshots, no
#                  view hierarchy, no database/file/network spans; the SAME "Analytics" switch
#                  stops it (CrashReporting.applyAllowed), hence single_switch
#   - storekit   : the occasional rating prompt after successful scans, and "Rate Us"
# Keep this in step with the App Privacy label in App Store Connect and with
# idscanner/PrivacyInfo.xcprivacy: adding or removing an SDK means updating all three.
services: [idscan, icloud, revenuecat, posthog, sentry, storekit]

idscan_retention_days: 90
content_description: "the scan history described below, your VIP and Banned lists, your notes and your settings"

icloud_default_off: true
icloud_content: "What syncs: the saved scans, the VIP and Banned lists with their notes, and the Minimum Age, Auto-Close, Keep Screen On and People Counter settings. While syncing is on, the random value used to make the one-way code (see above) is kept in iCloud Keychain, so a guest on your VIP or Banned list is recognised on each of your devices. Deleting scans or removing a guest on one device deletes them from your iCloud and from your other devices. The language, the Haptics and Analytics settings and the daily count of free scans stay on each device."

analytics_opt_out: true
crash_opt_out: true
single_switch: true

posthog_events_text: "a small set of events that mark steps in using the App: finishing the welcome pages (with whether camera access was allowed); the first scan on the installation (how it was read and its result category, such as valid or underage); once a day, a summary of the previous day’s scans that contains counts only (how many were read from a barcode or a passport or typed in, and how many had each result); the Unlimited screen being shown or closed, a purchase being started, completed, cancelled or failing (with a short reason such as a network problem), and the result of restoring purchases, each with which part of the App opened the screen; a problem with iCloud sync (its category); and the App being installed, opened, updated or closed. Nothing about the people whose IDs are scanned is ever sent: no name, gender, age, date of birth, ID number or code, issuer, note or list entry. We do not record which screens you view or which controls you tap, and we never send prices, receipts or your Apple Account to PostHog."
posthog_context_text: "basic technical context: app version, device model, operating system version, the minimum age set in the App, whether iCloud sync is on, and whether you have Unlimited. Your IP address reaches PostHog’s servers as part of any internet connection, but PostHog is set to discard it, and the App tells PostHog not to work out a location from it."

sentry_identifier_text: "a random technical identifier that Sentry’s software may generate for the installation, so that repeated reports from one device can be grouped. No name, email address or account identifier is attached to a report, and this identifier is not your Apple Account or your advertising identifier;"
sentry_extra:
  - "a few recent app events leading up to the failure, for example the App moving to the background;"
  - "anonymous session start and end markers, so we can measure how many sessions end in a crash;"
  - "reports of the App freezing or being ended by the system, and the diagnostics iOS itself makes when the App freezes or uses unusually much processor time or storage writing (stack traces and counts only);"
  - "for a sample of sessions, performance measurements: how long the App took to start and to show a screen, and how many frames were slow or frozen. They contain timings and the names of parts of the App’s code, never what is on the screen;"
  - "for a few errors that are not crashes, such as iCloud sync failing, a fixed error name and an error code, never the error’s message or any record."
---

{% include privacy/body.html %}
