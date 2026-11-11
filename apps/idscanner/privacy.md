---
layout: legal
permalink: /idscanner/privacy/
title: Privacy Policy
app_name: ID Scanner
effective: 2026-11-11

# What the app actually ships (checked against the code on 11 Nov 2026):
#   - no server, no analytics, no crash SDK, no ads, no tracking, no purchases
#   - idscan   : camera reads PDF417 barcodes and passport MRZ lines on device;
#                saved fields, never-saved fields, salted SHA-256 code, VIP/Banned
#                lists, 90-day default retention, CSV export, support email drafts
#   - storekit : "Rate the App" in Settings asks iOS to show the rating prompt
# Keep this in step with the App Privacy label in App Store Connect.
services: [idscan, storekit]

idscan_retention_days: 90
content_description: "the scan history described below, your VIP and Banned lists, your notes and your settings"
---

{% include privacy/body.html %}
