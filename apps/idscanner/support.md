---
layout: legal
permalink: /idscanner/support/
title: Support
app_name: ID Scanner
effective: 2026-11-18
---

<p>
  Something not working, an ID that would not scan, or an idea for the app? Write to us —
  the same person who builds the app reads the mail.
</p>

<p style="font-size:1.15rem">
  <a href="mailto:{{ site.support_email }}?subject={{ page.app_name | uri_escape }}%20Support"><strong>{{ site.support_email }}</strong></a>
</p>

<p>
  We aim to reply within two business days. Tapping <em>Contact Support</em> or
  <em>Request a Feature</em> in the app’s Settings fills in the app version, iOS version and
  device model for you. Please do not send photos of real IDs or the names of the people
  you scanned.
</p>

<h2>Common questions</h2>

<h3>Which IDs can it read?</h3>

<p>
  Driver licenses and ID cards from the United States and Canada that have a PDF417
  barcode on the back, and passports and passport cards. For anything else, tap
  <em>Enter Date of Birth</em> and type the date shown on the ID.
</p>

<h3>Can it tell me whether an ID is fake?</h3>

<p>
  No. ID Scanner checks the date of birth, the expiration date and whether the data is
  consistent. It cannot confirm that an ID is real or that it belongs to the person
  holding it. Look at the ID and compare the photo yourself.
</p>

<h3>An ID will not scan</h3>

<p>
  Hold the barcode steady inside the frame, tilt the card if light reflects off it, and
  turn on the flashlight in the dark. For a passport, point the camera at the lines of
  letters and “&lt;” signs at the bottom of the photo page. A worn or scratched barcode may
  not read at all; use <em>Enter Date of Birth</em> instead. If one kind of ID never reads,
  tell us which state, province or country issued it.
</p>

<h3>What do the results mean?</h3>

<ul>
  <li><strong>Valid</strong> — old enough, and the ID has not expired.</li>
  <li><strong>VIP</strong> — valid, and the guest is on your VIP list.</li>
  <li><strong>Underage</strong> — younger than the minimum age you set (the card shows it, for example “Under 21”).</li>
  <li><strong>Expired</strong> — old enough, but the ID has expired.</li>
  <li><strong>Suspicious</strong> — some of the data looks wrong, for example a date of birth in the future, an age over 100, an issue date after the expiration date or a missing field. Check the ID by hand.</li>
  <li><strong>Fake</strong> — the data in the barcode contradicts itself, or the same ID number was scanned before with a different name. Check the ID by hand.</li>
  <li><strong>Banned</strong> — the guest is on your Banned list.</li>
</ul>

<h3>The camera screen says access is needed</h3>

<p>
  Open <em>Settings → ID Scanner</em> on your device and turn on <em>Camera</em>. If the
  switch cannot be changed, camera use is restricted on the device, for example by Screen
  Time or by an organisation’s device management. On iPad, the camera works only while
  ID Scanner fills the whole screen.
</p>

<h3>How many scans are free?</h3>

<p>
  10 a day. Barcode scans, passport scans and dates of birth entered by hand all count;
  reading the same ID again within a few seconds does not. The count starts again at
  midnight. <em>Unlimited</em>, a weekly or yearly subscription, removes the limit.
  Everything else in the app is free. See the
  <a href="{{ '/idscanner/terms/' | relative_url }}">Terms of Use</a> for the details.
</p>

<h3>I paid for Unlimited, but the app still shows the daily limit</h3>

<p>
  Open <em>Settings</em> in the app and tap <em>Restore Purchases</em>, using the same
  Apple Account you subscribed with. Once Unlimited is active, the app keeps working
  without an internet connection until the end of the period you paid for.
</p>

<h3>How do I cancel Unlimited?</h3>

<p>
  In the app, open <em>Settings → Manage Subscription</em>, or on your device open
  <em>Settings → [your name] → Subscriptions</em>. Cancelling stops the next renewal; you
  keep Unlimited until the end of the period you paid for. Refunds are handled by Apple at
  <a href="https://reportaproblem.apple.com">reportaproblem.apple.com</a>.
</p>

<h3>Where is the scan history stored, and for how long?</h3>

<p>
  On your device, and in your own iCloud account if you turn on <em>iCloud Sync</em> in
  Settings (it is off by default). Saved scans are deleted automatically after 90 days. To
  delete one scan, swipe it in the History screen. You can also delete scans from today,
  the last 7 days, the last 30 days or all time from the History screen. The <a href="{{ '/idscanner/privacy/' | relative_url }}">Privacy
  Policy</a> lists exactly what is saved and what never is.
</p>

<h3>My scans and VIP and Banned lists are not on my other device</h3>

<p>
  Turn on <em>iCloud Sync</em> in Settings on each device, then close and reopen ID
  Scanner. Both devices must be signed in to the same iCloud account, with iCloud Keychain
  on, so that guests on your lists are recognised on both. Without iCloud Sync, a guest is
  recognised only on the device where they were added.
</p>

<h3>What does the Analytics switch do?</h3>

<p>
  It sends anonymous usage statistics (for example how many scans were made each day,
  counts only) and crash reports, which help us fix problems. Nothing about the people
  whose IDs you scan is ever sent. It is on by default; turn it off in
  <em>Settings → About Us → Analytics</em> and nothing more is sent. See the
  <a href="{{ '/idscanner/privacy/' | relative_url }}">Privacy Policy</a>.
</p>

<h3>My ID was scanned with ID Scanner. Who has my information?</h3>

<p>
  The person or business that scanned it. The record is on their device, and in their own
  iCloud account if they use iCloud Sync. We cannot see or delete it. Ask them. See
  <a href="{{ '/idscanner/privacy/' | relative_url }}">the Privacy Policy</a>.
</p>

<h2>Legal</h2>

<ul>
  <li><a href="{{ '/idscanner/privacy/' | relative_url }}">Privacy Policy</a></li>
  <li><a href="{{ '/idscanner/terms/' | relative_url }}">Terms of Use</a></li>
</ul>
