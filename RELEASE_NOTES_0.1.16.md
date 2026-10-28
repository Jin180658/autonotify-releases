# AutoNotify 0.1.16

Windows installer with bundled Node.js and PostgreSQL. No manual development setup or cloud hosting is needed.

## Install or upgrade

Download **AutoNotify-Setup-0.1.16.exe** below. New users should follow the [installation and Gmail setup guide](https://github.com/Jin180658/autonotify-releases#install).

Existing users: create a backup, then use the in-app update or run this installer under the same Windows account. Your local account, customer records and email settings are retained. Do not delete the data folder.

## Changes since the previous public release (0.1.5)

- English and Simplified Chinese interface, selectable in Settings or before sign-in.
- Simpler navigation: Dashboard, Customers, Renewals and Email History; setup tools grouped in Settings.
- Verified-email administrator setup and email-code password recovery, with optional offline recovery codes.
- Customer remarks, customer overview, multiple-vehicle management and optional VEP ID.
- Policy paperwork: premiums, stamp duty, road tax, service/extra charges, payment totals and balances.
- Independent Road Tax, Insurance, VEP and P.A. reminders, so one expired policy does not hide another upcoming expiry.
- Dashboard reminder operation status, clearer forms/validation, focused renewals and consolidated CSV export.
- Password-encrypted full backups and guided restore; restored reminders pause for review.
- Improved migration/startup safeguards and version-aware in-app update progress.
- Email-only delivery using Gmail, with optional Resend configuration. SMS and WhatsApp have been removed.

## Before relying on automatic sending

Keep both recommended startup/reminder options checked, configure your own Gmail App Password, and send a test email. The laptop must be on, signed into Windows and online. Provider acceptance does not guarantee inbox delivery. Update each renewed policy's date and keep off-laptop backups.

UI language does not translate customer data, CSV exports or outgoing emails.

## Verification and remaining acceptance

155 unit tests, 15 PostgreSQL integration tests, lint, production build, translation audit, disposable production browser checks and an upgrade of the existing local installation passed. A fresh second-PC installation, reboot trial and genuinely newer public in-app update still need real-user acceptance testing. Start with one trial laptop.

## Installer checksum

SHA-256 (`AutoNotify-Setup-0.1.16.exe`, 57,945,710 bytes):

```text
144868B2BF47A4D66F0269B47DB924D4B9D99FE5B2F58BFF73F69A9C5FBCC903
```
