---
layout: legal
permalink: /habitgrid/privacy/
title: Privacy Policy
app_name: HabitGrid
effective: 2026-09-04

# Only the services listed here are described on the page. This list now matches
# what the app actually ships:
#   - revenuecat : HabitGrid Pro auto-renewable subscription (added 3 Sep 2026)
#   - posthog    : product analytics, PostHog EU cloud, anonymous — no identify,
#                  no person profiles, no habit content (see AnalyticsService.swift)
#   - sentry     : crash and error reporting, Sentry DE region, sendDefaultPii off
# Keep this in step with the App Privacy label in App Store Connect: adding or
# removing an SDK here means updating the label in the same submission.
services: [icloud, notifications, storekit, revenuecat, posthog, sentry]

icloud_default_off: true
in_app_export: true
in_app_erase: false
content_description: "your habits, their names, icons and colours, your completion history, reminders and settings"
---

{% include privacy/body.html %}
