# AutoNotify Releases

This is the official public download page for AutoNotify. It contains installer releases and the update manifest used by installed copies to detect a newer version.

> This repository intentionally contains **no application source code, customer data, database backup, environment file, or credentials**.

## Install AutoNotify

1. Open the [latest release](https://github.com/Jin180658/autonotify-releases/releases/latest).
2. Under **Assets**, download the file named `AutoNotify-Setup-<version>.exe`. Do not download the source-code ZIP or TAR files.
3. Double-click the downloaded installer.
4. Keep these recommended options selected:
   - **Start AutoNotify when I sign in to Windows** — keeps the local app ready after the laptop starts.
   - **Run the daily reminder check at 9:00 AM** — sends due reminders and eligible catch-up reminders without manually opening AutoNotify.
5. Choose the installation folder if you do not want the default location.
6. When installation is complete, open **AutoNotify** from the Windows Start Menu or the Desktop shortcut. The shortcut starts the local service and opens the app in your default browser.

## First-time setup

1. Create the one-time local admin password.
2. Keep the recovery code in a safe place. It is needed if the password is forgotten.
3. Go to **Profile Settings → Gmail reminder delivery** and enter the Gmail address, sender name, and a Google App Password.

AutoNotify keeps its customer data, local database, and delivery settings on the same Windows user account. Updating or uninstalling the program does not remove that data.

## Automatic reminders

When the recommended daily task is enabled, AutoNotify checks active vehicle policies each day at 9:00 AM. It sends configured email/SMS reminders only for eligible expiry windows and avoids duplicates. If the PC was off, eligible missed pre-expiry reminders can be caught up when AutoNotify next runs; expiry-day reminders are not sent late.

## Updates

When a newer release is published here, installed AutoNotify copies show an update link inside the application. Select it to download the new installer, then run the installer normally. Your local data and settings remain in place.

## Current release

Download the current installer from the [latest release](https://github.com/Jin180658/autonotify-releases/releases/latest).
