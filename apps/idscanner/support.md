---
layout: legal
permalink: /idscanner/support/
title: Support
app_name: ID Scanner
effective: 2026-11-11
---

<p>
  Something not working, or an ID that would not scan? Write to us — the same person who
  builds the app reads the mail.
</p>

<p style="font-size:1.15rem">
  <a href="mailto:{{ site.support_email }}?subject={{ page.app_name | uri_escape }}%20Support"><strong>{{ site.support_email }}</strong></a>
</p>

<p>
  We aim to reply within two business days. Tapping <em>Contact Support</em> in the app’s
  Settings fills in the app version, iOS version and device model for you. Please do not
  send photos of real IDs.
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
  open the scan in History, tap the “…” button and choose <em>Report a Problem</em>.
</p>

<h3>What do the results mean?</h3>

<ul>
  <li><strong>Pass</strong> — old enough, and the ID has not expired.</li>
  <li><strong>Under</strong> — younger than the minimum age you set.</li>
  <li><strong>Expired</strong> — old enough, but the ID has expired.</li>
  <li><strong>Check ID</strong> — the data looks wrong, for example an age over 100 or a missing field. Check the ID by hand.</li>
  <li><strong>Banned</strong> and <strong>VIP</strong> — the guest is on one of your lists.</li>
</ul>

<h3>The camera screen says access is needed</h3>

<p>
  Open <em>Settings → ID Scanner</em> on your device and turn on <em>Camera</em>. If the
  switch cannot be changed, camera use is restricted on the device, for example by Screen
  Time or by an organisation’s device management.
</p>

<h3>Where is the scan history stored, and for how long?</h3>

<p>
  On your device only. Saved scans are deleted automatically after 90 days unless you
  change <em>Auto-Delete After</em> in Settings. You can turn <em>Save History</em> off,
  delete scans from the History screen, or use <em>Delete All History</em>. The
  <a href="{{ '/idscanner/privacy/' | relative_url }}">Privacy Policy</a> lists exactly
  what is saved and what never is.
</p>

<h3>I moved to a new device and my VIP and Banned guests are not recognised</h3>

<p>
  Guests are recognised by a one-way code that only works on the device that made it. On
  a new device restored from a backup, the lists may still show the names but a scan will
  not match them. Mark the guest again the next time you scan their ID.
</p>

<h3>My ID was scanned with ID Scanner. Who has my information?</h3>

<p>
  The person or business that scanned it. The record is on their device and we cannot see
  or delete it. Ask them. See
  <a href="{{ '/idscanner/privacy/' | relative_url }}">the Privacy Policy</a>.
</p>

<h2>Legal</h2>

<ul>
  <li><a href="{{ '/idscanner/privacy/' | relative_url }}">Privacy Policy</a></li>
  <li><a href="{{ '/idscanner/terms/' | relative_url }}">Terms of Use</a></li>
</ul>
