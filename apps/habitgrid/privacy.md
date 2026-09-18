---
layout: legal
permalink: /habitgrid/privacy/
title: Privacy Policy
app_name: HabitGrid
effective: 2026-09-09

# Only the services listed here are described on the page. This list now matches
# what the app actually ships:
#   - revenuecat : HabitGrid Pro auto-renewable subscription (added 3 Sep 2026)
#   - posthog    : product analytics, PostHog EU cloud, anonymous — no identify,
#                  no person profiles, no habit content; opt-out, on by default
#                  (see AnalyticsService.swift + PrivacyConsent.swift)
#   - sentry     : crash and error reporting, Sentry DE region, sendDefaultPii
#                  off; opt-out, on by default
# Keep this in step with the App Privacy label in App Store Connect: adding or
# removing an SDK here means updating the label in the same submission.
services: [icloud, notifications, storekit, revenuecat, posthog, sentry]

icloud_default_off: true
# As of 9 Sep 2026 both analytics and crash reporting are ON by default, on the
# GDPR legitimate-interest basis (all anonymous — no identify, sendDefaultPii
# off, EU hosts). Settings has two switches — "Share Usage Data" (analytics) and
# "Crash Reports" — that withdraw it, and a decline from the earlier opt-in
# prompt is still honoured. These two flags render "legitimate interest +
# opt-out" rather than "consent". See SettingsView + PrivacyConsent.swift.
#
# 18 Sep 2026: the one-time in-app notice that used to follow onboarding was
# removed. Nothing required it — App Review 5.1.1(ii) asks for a way to withdraw
# (the two switches) and a Privacy Policy that explains it (this page) — and HIG
# Alerts > Best practices rules out an informational alert at launch. THIS PAGE IS
# NOW THE ONLY DISCLOSURE, so the Art. 13 detail below has to stay accurate.
analytics_opt_out: true
crash_opt_out: true
in_app_export: true
in_app_erase: false
content_description: "your habits, their names, icons and colours, your completion history, reminders and settings"
---

{% include privacy/body.html %}
