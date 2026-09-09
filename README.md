# Legal pages

Privacy policies, terms of use and support pages for my iOS apps, published with
GitHub Pages at **<https://cevatakdemir21.github.io/legal/>**.

The point of this repo is that the text is written once and each app switches on
only the sections that are true for it. An app's page never claims a service the
app does not actually use — which is what App Store Review Guideline 5.1.1(i)
asks for, and what makes the App Privacy label on App Store Connect defensible.

There is no build step to run locally. GitHub Pages builds the Jekyll site on
push.

---

## Adding a new app

Create `apps/<slug>/privacy.md`, `terms.md` and `support.md`. A whole privacy
policy is front matter plus one line:

```yaml
---
layout: legal
permalink: /myapp/privacy/
title: Privacy Policy
app_name: MyApp
effective: 2026-09-01
services: [icloud, revenuecat, posthog, sentry]
icloud_default_off: true
analytics_opt_out: true
crash_opt_out: true
content_description: "the notes you write, your tags and your settings"
---

{% include privacy/body.html %}
```

Then add the app to `index.md`, and point the app's in-app Privacy Policy and
Terms of Use links (and App Store Connect's Privacy Policy URL and Support URL)
at the new permalinks.

## Privacy front matter

`services:` decides which sections appear. Include only what the app really does.

| value | section emitted |
|---|---|
| `icloud` | CloudKit sync into the user's own private database |
| `notifications` | Local notifications scheduled on device |
| `storekit` | App Store ratings and reviews |
| `posthog` | Product analytics |
| `sentry` | Crash and error reporting |
| `revenuecat` | Purchases and subscriptions |
| `supabase` | Hosted content — explicitly *not* accounts or auth |

The intro and the on-device-storage section are always emitted, as is the tail
(legal bases, retention, deletion, children, GDPR/KVKK/CCPA rights, transfers,
security, changes, contact).

Supporting flags:

| flag | effect |
|---|---|
| `content_description` | Names what the app stores, in the on-device section. Worth setting — the default is vague. |
| `icloud_default_off: true` | States that sync is opt-in. Only set it if that is true. |
| `in_app_export: true` | Mentions the app's own export/import. |
| `in_app_erase: true` | Adds "use the erase option in Settings" to the deletion list. |
| `analytics_opt_out: true` | Analytics is on by default, legitimate interest is the basis, and it can be turned off in-app. Only set it if that switch exists. Leave it unset for an opt-in app — then consent is the basis. |
| `crash_opt_out: true` | Same, for crash reporting: says it is on by default and can be turned off in the App's settings. |
| `supabase_writes: true` | Says the app also *sends* data to Supabase, not just reads. |
| `supabase_purpose`, `supabase_description`, `supabase_written_data` | Wording for the Supabase section. |

## Terms front matter

```yaml
privacy_url: /myapp/privacy/   # linked from the Terms
has_iap: true                  # adds the purchases section
has_subscriptions: true        # adds auto-renewal / cancellation terms
has_accounts: false            # adds account-security + in-app deletion clause
has_ugc: false                 # adds content moderation clause
```

The Terms double as the EULA and reference Apple's standard
[Licensed Application End User License Agreement](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/),
which is the arrangement Guideline 3.1.2 expects. They also carry the
Apple-required third-party-beneficiary and export-compliance clauses.

**If the app sells subscriptions, set `has_iap` and `has_subscriptions` to
`true` and link both the Terms and the Privacy Policy from the paywall screen
itself** — not only from Settings. Guideline 3.1.2 rejections are usually about
the paywall, not the settings screen.

## Checklist when an app changes

- Added a new SDK? Add it to `services:` and update the App Privacy label on App
  Store Connect in the same session — the two must agree.
- Removed one? Take it out of `services:` too.
- Any material change: bump `effective:` on the page.

## Files

```
_config.yml                developer name, support email, jurisdiction
_layouts/legal.html        page chrome for a policy page
_layouts/home.html         page chrome for the index
_includes/privacy/body.html   the switchboard — reads `services:`
_includes/privacy/*.html      one file per section
_includes/terms/body.html     the terms, with the flags above
apps/<slug>/*.md           one folder per app
assets/style.css           the only stylesheet
```
